# Deploy-Web-App
Deploy Web Application Using Nginx on Ubuntu
First Install Nginx on your device by this command  "sudo apt-get install nginx"
Make sure you enable your firewall by this command  "sudo ufw enable"
Enable nginx full ports by this command  " sudo ufw allow 'Nginx Full' "
Check your nginx is active by this command  "sudo systemctl status nginx"
Next copy your demo file your Web application to " /var/www " if you are using ubuntu
Next go to your /etc/hosts Add an IP address with domain name for example "ip: 0.0.0.0    domainame: Demo.com"
next add some permissions to your demo file so we can copy it to your server by using this command  "sudo chmod -R 777 * "
now copy your demo file to the server by using this command    "scp -r * 0.0.0.0:/var/www/demo"
Next Create a Config file in "sudo nano etc/nginx/sites-available/demo" and copy the "configuration file" 
After you copy this configuration save it and then copy it to sites enable using this command "sudo ln -s /etc/nginx/sites-available/demo /etc/nginx/sites-enable/demo"
finally move your default file in sites enable to another direcatory by this command "sudo mv /etc/nginx/sites-enabled/default /home
restart your nginx "sudo systemctl reload nginx"
