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
I then reload the httpd
