# react_django_demo_app
A demo app for React and Django Deployment

- Fork this repository
- Run 'ssh-keygen' to generate SSH key-pair.
- Add 'id_rsa.pub' to Github Settings --> SSH and GPG keys. Select key type as "Authentication keys"

## Configuring Jenkins
- Select New Item
- Add name of the item and select Freestyle project
- In the Configure page, add github url.
- In SCM, add github url, repository branch and in credentials, add private key.
- Under "Build Trigger" select "GitHub hook trigger for GITScm pollling".
- Under "Build Steps" , select "Execute Shell" and add an echo statement and click "Save".


## Configuring Jenkins webhook in github
- In your git repository, go to "settings" and then "Webhooks".
- Click "Add webhook" button. The payload url will be "http://<Jenkins-url>/github-webhook/". Click on Add webhook.
  
## Build the project
- Go to your jenkins dashboard, Configure --> Build Steps --> Execute shell.
- Add the following commands: 
 'docker-compose down'
 'docker-compose up -d'
- Save and build the project.
- Verify whether build is successful.
- Browse public IP address with port 8001

  
