# simple-cicd-ec2
Demo for implementing a simple CI/CD pipeline at AWS ECC2 using Ansible|Jenkins|Docker

::Steps::

- Deploy 3 EC2 instances (Ansible,Jenkins & WebServer)
- Deploy Playbooks to set up each of the above
- Create Pipeline in Jenkins
- Deploy the simple-website from `https://github.com/BINPIPE/simple-website` via the simple pipeline.

Once comfortable you can add it up with steps like Sonarscan, Monitoring & using Declarative pipelines later on. You can also try containerising the Website using Docker and deploy it using Docker containers!
