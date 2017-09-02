# phpstorm-php56template
Template project for PHP5.6 development with PHPStorm and Docker

Usage:
 - Clone Template
 - Change port mapping in docker-compose.yml if necessary
 - Setup Docker in File -> Settings -> Build, Execute, Deployment -> Docker
 - Create/edit Run Configuration in Run -> Edit Configuration -> Docker Deployment
   - Give it a name (i.e: Start Docker)
   - Choose server set up above and deployment: docker-commpose.yml
 - Deploy the new Docker Deployment to initiallize the Images and such
 - Create php executable in File -> Settings -> Languages & Frameworks -> PHP
   - use From Docker, Vagrant, VM, Remote... -> Docker Compose 
     - if you are on windows change the enviroment settings to not include parent environment
 - Change the Templatee index - website/index.php