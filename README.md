# PROJECT-9
Tooling Website deployment automation with Continuous Integration, Intro to Jenkins
Step 1 – Install Jenkins server

1. Create an AWS EC2 server based on Ubuntu Server 20.04 LTS and name it "Jenkins"

2. Install JDK (since Jenkins is a Java-based application)

sudo apt update
sudo apt install default-jdk-headless

![image](https://user-images.githubusercontent.com/113097621/217717498-3b84e0cd-8d52-42b4-b260-720cf0212e05.png)

![image](https://user-images.githubusercontent.com/113097621/217717811-18d2f4dd-eb1d-449e-80af-1a36a5ad9804.png)


3. Install Jenkins
![image](https://user-images.githubusercontent.com/113097621/217718862-cc534ef9-87bc-42b2-9bdf-70b2d16da92f.png)

Make sure Jenkins is up and running

![image](https://user-images.githubusercontent.com/113097621/217725103-5e5d97e7-c630-4db0-ac0c-d2ed2c22f3b3.png)

4. By default Jenkins server uses TCP port 8080 – open it by creating a new Inbound Rule in your EC2 Security Group

![image](https://user-images.githubusercontent.com/113097621/217725322-eb930cc6-2aa3-4fef-8629-b16683ea1d26.png)

5. Perform initial Jenkins setup.
http://<Jenkins-Server-Public-IP-Address-or-Public-DNS-Name>:8080
    
![image](https://user-images.githubusercontent.com/113097621/217725516-a2fa628a-61c7-424f-adf5-1958e54fc53a.png)

![image](https://user-images.githubusercontent.com/113097621/217726028-e2565f54-0615-4827-aaf4-f46d3d224340.png)

![image](https://user-images.githubusercontent.com/113097621/217726137-f9e00e23-d2f5-40a0-b6e9-3fc8329aa419.png)

    
STEP 2
    Configure Jenkins to retrieve source codes from GitHub using Webhooks
    Enable Webhooks in your GitHub repository settings
    
    Connect to GitHub Repository by copying the URL
    ![image](https://user-images.githubusercontent.com/113097621/217968850-1337afaf-ae43-4203-a8c4-d742c198c1b0.png)
![image](https://user-images.githubusercontent.com/113097621/217970664-cce9e451-7c42-4720-bfb9-2809ef825c78.png)

Console Output
![image](https://user-images.githubusercontent.com/113097621/217985032-3e0b2888-18ba-4498-942c-9fce5db19488.png)


    Add the line Checking Jenkins
    ![image](https://user-images.githubusercontent.com/113097621/217993540-5d71657a-39c0-4ec3-a54b-101361fac5fb.png)

   By default, the artifacts are stored on Jenkins server locally 
    ![image](https://user-images.githubusercontent.com/113097621/217996744-eb636e33-6b89-489e-a1a5-78fe91a99de8.png)
    
    
    Configure Jenkins to copy files to NFS server via SSH
    
   Publish over SSH plugin was installed
    ![image](https://user-images.githubusercontent.com/113097621/217997805-118b0dc4-b961-4c3a-ab78-ec031d501944.png)

    
    Configure the job/project to copy artifacts over to NFS server.
    







