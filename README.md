# kuralabs_deployment_3
Deploying software to a VPC deployment 3 
<h3>See full documentation here >> <a href="https://github.com/Hobsonkp/kuralabs_deployment_3/blob/main/Documentation/KSmith_KURA3_Deployment3_20221018.pdf">KSmith_KURA3_Deployment3_20221018.pdf</a></h3>
<h1>Overview </h1>
This deployment exercise demonstrated the steps for setting up a basic CI/CD pipeline deployment to a custom AWS VPC.
Pipeline deployment
The software application used in this case was a Flask web application called “url shortener”
GitHub was used to manage the code and Jenkins was used to automate the following stages:
1.	Build
2.	Test
3.	Clean
4.	Deploy 
Issues:
There were issues encountered in the initial deployment due to:
1.	The configuration of the nginx server “/etc/nginx/sites-enabled/default” file. 
initial instructions:
 
 



The errors encountered included requesting browser not being able to access dependencies in subfolder (e.g. css files and js files)
correction: 







<a href="https://github.com/Hobsonkp/kuralabs_deployment_3/blob/main/Documentation/Deployment-3_Assignment%20(1).pdf">(See Deployment_3-Assignment page 11)</a>

2.	The script in the Jenkins file did not successfully allow the application to continue running at the end of a “successful” deployment.
Correction: download the Jenkins plugin “Pipeline Keep Running Step”
Use revised script in Jenkinsfile: <a href="https://github.com/Hobsonkp/kuralabs_deployment_3/blob/main/Documentation/Deployment-3_Assignment%20(1).pdf">(See Deployment_3-Assignment page 12)</a>

