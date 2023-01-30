import smtplib

sender_email = "sender@example.com"
receiver_email = "receiver@example.com"
password = "your_password"

message = """\
Subject: Auto Email Marketing Tool

This is a test email sent using Python's smtplib library.
"""

server = smtplib.SMTP('smtp.gmail.com', 587)
server.starttls()
server.login(sender_email, password)
server.sendmail(sender_email, receiver_email, message)
server.quit()
