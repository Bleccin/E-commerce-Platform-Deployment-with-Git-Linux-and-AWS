I created a directory called "MarketPeak_Ecommerce"
I moved into the directory and used "git init" to initialize a local git repository.
Downloaded and extracted the E-commerce Website Template codes into the "MarketPeak_Ecommerce" directory. 
I stagged the E-commerce website codes.
I committed the codes with this commit message "Initial commit with basic e-commerce site structure"
I created a Github repository called "MarketPeak_Ecomerce" 
Connected it to the local directory and pushed the codes from local directory into it.
I set Up an AWS EC2 instance using Amazon Linux AMI
The EC2 did no have git installed so I had to use sudo yum install git-all to install git on it.
I connected to the instance using ssh method of first generating a public key and adding the generated key to Github.
I cloned the git repository on the the EC2 instance.
I updated the Linux server and installed Apache HTTP Server (httpd) on the EC2 instance.
I started the web server and ensured it automatically starts on server boot.
I configured the httpd to point to the Linux server where the website code files are stored.
I then reload the httpd using sudo systemctl reload httpd.
I copied the public IP of the EC2 instance and pasted it in a browser which opened the e-commerce site to confirm that the website is now live on the internet. 
To practice continous integration and Development Workflow I created another git branch called "development" and checkout to it.
I made some changes to the HTML code, staged it and then committed it with the message "Add new features or fix bugs"
After that I pushed the changes into Github under a new branch named "development"
I created a Pull Request and merged the development branch into the main branch.
I then merged checkout to the "master" branch on the local repository and merged the "development" branch with it.
I then pushed the merged "master" branch into Github to ensure that the local main branch now contains the updates pushed to the remote repository on Github.
While doing this, I got an error saying that I must first pull an updated version from Github before pushing again. I did this and was able to push the merged branch into Github. 
I logged in back to the EC2 instance and then pulled the latest changes from GitHub into it.
I restarted Apache again with sudo systemctl reload httpd
I then used sudo rm -rf /var/www/html/* to remove the existing web service on Apache.
After which I used sudo cp -r ~/MarketPeak_Ecommerce/* /var/www/html/ to copy the updated code of the web service into the Apache directory.
I then tested this by reopening the public IP of the EC2 instance where I saw the update I made to the web service.
