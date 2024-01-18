# Cloud Architect Dicoding Final Project
## By Frico Simon

This project demonstrates a hands-on application of cloud architecture principles to create a functional and efficient cloud-based solution. It showcases a comprehensive understanding of Google Cloud Platform services and their potential to address real-world challenges.

### Key areas explored in this project include:

- Infrastructure design and deployment
- Resource management and optimization
- Security best practices
- Scalability and performance optimization
- Cost-effectiveness

### Cloud Architecture Overview

I implemented the following cloud architecture using Google Cloud Platform (GCP):

![GCP Architecture](https://github.com/FricoSimon/Cloud-Architect-Dicoding/blob/main/gcp%20architecture.png)

### First Step (Create a Project)
The first step is to create a new project in Google Cloud Platform (GCP) and don't forget to link a billing account to the project.

![Create a Project](https://github.com/FricoSimon/Cloud-Architect-Dicoding/blob/main/create%20project.png)

### Second Step (Create an Instance Group, Configure Auto Scaling, and Configure Load Balancer)
The second step consist of three parts as stated above

### - Create an Instance Group
I created 2 instance groups for two different region (Europe and Asia) and don't forget to create an instance template before create the instance group. The instance's machine type is n1-standard-4 as the server will be used for e-commerce sites. The specification is set not too high and not too low to maintain the performance.

![Create an Instance Group](https://github.com/FricoSimon/Cloud-Architect-Dicoding/blob/main/instance%20group.png)

### - Configure Auto Scaling
Next is to set auto scaling to the instance group so our MIG (Managed Instance Group) can scale automatically. The minimum instance is one so the server will always be ready to receive request from users, The maximum instance is two to keep the cost under limit. The CPU Utilization is set to 60% and the initialization period to 60 seconds.

![Configure Auto Scaling](https://github.com/FricoSimon/Cloud-Architect-Dicoding/blob/main/configure%20auto%20scaling.png)

### - Configure Load Balancer
Last is to set load balancer, the purpose is to keep the load balance to all the instances in MIG. The load balancer that I used is Application Load Balancer (HTTP/S) with Global external Application Load Balancer. By effectively distributing traffic and ensuring high availability, the load balancer plays a vital role in the overall performance and reliability of the cloud architecture.

![Configure Load Balancer](https://github.com/FricoSimon/Cloud-Architect-Dicoding/blob/main/configure%20load%20balancer.png)

### Third step (Create Custom Dashboard for Monitoring)
After everything's done, We have to create a custom dashboard to help us monitor and maintain the cloud project. It's really useful for us, because we can regularly check on the server status, etc. In this custom dashboard, I included four different metrics: instance group size (compute engine), CPU utilization (Mean), Load Balancer request count, and VM instances send byte (sending response to outside). We can add more metrics if needed, but for now it's already enough.

![Create Custom Dashboard](https://github.com/FricoSimon/Cloud-Architect-Dicoding/blob/main/create%20custom%20dashboard%20for%20monitoring.png)
