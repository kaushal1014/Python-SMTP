import smtplib
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText
from email.mime.base import MIMEBase
from email import encoders

# sender
fromadd = ""
# receiver
toadd = ""
msg = MIMEMultipart()
msg['from'] = fromadd
msg['to'] = toadd
# subject
msg["subject"] = ""
body = "body_of_mail"
msg.attach(MIMEText(body, "plain"))
#path of the file
filename = ""
# open file in read and binary mode
attachment = open(filename, "rb")
p = MIMEBase("application", "octet-stream")
p.set_payload(attachment.read())
encoders.encode_base64(p)
p.add_header("Content-Disposition", "attachment; filename=" + filename)
msg.attach(p)
# 587 is the port
mainserver = smtplib.SMTP('smtp.gmail.com', 587)
mainserver.starttls()
# senders gmail and password
mainserver.login(fromadd, "")
text = msg.as_string()
mainserver.sendmail(fromadd, toadd, text)
mainserver.close()
