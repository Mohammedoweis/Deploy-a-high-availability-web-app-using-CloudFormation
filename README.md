# Deploy-a-high-availability-web-app-using-CloudFormation
this project about Deploy a high-availability web app using CloudFormation
http://my-se-webap-v1075ugv7k39-1294961041.us-east-1.elb.amazonaws.com/ this is the link for website 
Project Overview

Infrastructure Diagram:
![Flowcharts](https://user-images.githubusercontent.com/109382355/189526936-eff34244-dd42-4d38-a91e-e89004bd5b0b.png)



#Project Setup

    To create networking resources using cloudformation template, run the below command. After exceuting it these are the resources created:

    VPC
    Subnets
    Route Tables
    Routes
    Internet Gateway
    NAT Gateways

$ scripts/create.sh webapp-network-stack network.yml network-params.json

    To create servers resources using cloudformation template which pulls source code from S3 bucket automatically while starting, run the below command. After exceuting it these are the resources created:

    Security Groups
    IAM Role, Policy, Instance Profile
    Launch configuration
    Auto Scaling Group
    Load Balancer
    Target Group

$ scripts/create.sh webapp-server-stack server.yml server-params.json

Once the above steps are complete, you can find the URL of application in the outputs section of udagram-servers-stack CloudFormarion stack.
