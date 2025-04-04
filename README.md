# logsentry
emails alerts for failed login attempts on Debian systems 

Looks at /var/log/auth.log which requires rsyslog to be enabled on the system. 
Uses msmtp with gmail for the reporting, so a config with .msmtprc has to be done. 
              defaults
        auth           on
        tls            on
        tls_trust_file /etc/ssl/certs/ca-certificates.crt
        logfile        ~/.msmtp.log
        
        account        gmail
        host           smtp.gmail.com
        port           587
        from           your.email@gmail.com
        user           your.email@gmail.com
        password       your_app_password_here
        
        account default : gmail
