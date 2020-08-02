#By kaushal Patil
import smtplib

u=input("enter the senders email:")
p=input("enter the senders email password:")
r=input("enter the receivers email:")
m=input("enter the meassage or content:")
sender= u
password =p
receiver = r
meassage =m
mainserver = smtplib.SMTP('smtp.gmail.com', 587)

mainserver.starttls()
mainserver.login(sender, password)
mainserver.sendmail( sender, receiver,meassage)
mainserver.close()
