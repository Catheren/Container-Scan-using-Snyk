# Container-Scan-using-Snyk

Snyk is a security platform designed to help organizations find and fix vulnerabilities in their code, open-source dependencies, container images, and infrastructure as code (IaC).
We will use Snyk to scan Docker images to identify vulnerabilities in this section. Hence, we need to install both Docker for Windows and Snyk CLI for Windows on the local machine. 

To install Docker:
1. Go to https://docs.docker.com/desktop/install/windows-install/ and download the executable file.
2. Install it on your local machine.
3. To check if Docker is running successfully, run the following on Command Prompt. 
```
docker --version
```

To install Snyk CLI for Windows: 
1. Go to this [repository](https://github.com/snyk/cli/releases) and download the executable file for Windows.
2. Install it to the desired folder.
3. Open Command Prompt from the location you have installed Snyk.
4. Authenticate to Snyk using the following command:
```
snyk-win.exe auth
```
  This will be redirected to the Snyk authentication page on your browser.
  ![image](https://github.com/Catheren/Container-Scan-using-Snyk/assets/94724571/3ce1aa97-d7ab-476d-82fb-299ee5276f68)

5. Pull the required docker image you want to scan from Docker Hub. I am pulling the python:3.4-alpine.
   ```
   docker pull python:3.4-alpine
   ```
   ![image](https://github.com/Catheren/Container-Scan-using-Snyk/assets/94724571/babaf49c-fbc5-4f1b-a869-b726ec0b6365)
6. Run the following command to test the docker container using Snyk:
   ```
   snyk-win.exe container test python:3.4-alpine
   ```
   This will provide the scan results identifying all the vulnerabilities of the docker image and the alternative recommendations.
   

