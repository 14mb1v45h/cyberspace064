# PyPhisher

A simple python tool for phishing

## Installation
```
python3 -m pip install -r requirements.txt
```

## Description
This tool was created for the purpose of phishing during a penetration test./redteam operation. I wanted to create command line tool (to allow for automation) that would take a pre-crafted html email file then replace all the links and send the email. The replacing of links was something I was previously doing manually.

## Usage

**Requirements:**

* SMTP server (Usually runs on port 25)
* Username and Password (For the SMTP server)

```
PhishCrypt.py --server <mail_server> --port <port> --username <user> --password <password> --html <html_phish> --url_replace <replace_url> --subject <subject> --sendto <email> --list-sendto <list_of_emails> --attachment <attachment_file>
```

## Example
```
PhishCrypt.py --server mail.server.com --port 25 --username user --password password --html phish.txt --url_replace phishlink.com --subject Read!! --sender important@phish.com --sendto target@company.com --list-sendto list_emails.txt --attachment somepdffile.pdf
```

## Available options
```
--server          The SMTP server that you are going to be using to send the email
--port            The port number that is setup for SMTP
--html            The pre-crafted html that will be used in the email
--url_replace     The url that will be used to replace all links in the email
--subject         The subject that will appear in the email message
--sender          The sender that will appear on the email example
--sendto          Who you would like to send the email to
--list-sendto     List of emails you wan to send email to (separated with \n)  
--start-tls       Will attempt to upgrade connection using SSL/TLS
--attachment      Path of the file you want to submit as an attachment
```

https://github.com/14mb1v45h/cyberspace064.git

AUTHOR - 14mb1v45h/cyberspace064