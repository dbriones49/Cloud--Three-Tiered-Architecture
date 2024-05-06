# Cloud-Three-Tiered-Architecture



## Introduction

XYZ company is a new company launching a global E-commerce business selling candles, and is in need of a robust cloud solution to host their website and handle the demands of online shopping. In order to ensure seamless operation, the cloud architecture must be scalable to accommodate fluctuations in website traffic, provide redundancy to prevent downtime, be reliable for uninterrupted service, and offer top-notch security to protect customer data. Additionally, the client is looking for benefits such as efficient data storage and caching to enhance website performance. In addition, they would like the solution to auto monitor the web server and handle the business logic and processing of customer orders such as invetory and payment processing. 

A three-tiered AWS cloud architecture is a design that separates the solution into three layers: presentation, application, and data. The presentation tier is responsible for the user interface, the application tier handles the business logic, and the data tier manages the storage and retrieval of data. 

The benefits of a three-tiered architecture include improved scalability, as each tier can be scaled independently based on demand. It also enhances security by isolating different functions and data, reducing the risk of unauthorized access. Additionally, it allows for easier maintenance and updates, as changes can be made to one tier without affecting the others.


For this design, I used two regions to ensure redundancy, and I included both private and public subnets within a VPOC.  The private subnet helps enhance security by isolating resources from the public internet, reducing the risk of unauthorized access or attacks. It also allows for better control over network traffic and ensures that sensitive data remains protected.

The Web Server will host the website, Amazon Aurora will be used for the data storage, AWS Identity and Acess management will provides granular control over access to resources, and Elastic Beanstalk will be used to auto manage the server and process payments, and AWS Cloudfront will allow the business to distribute their web content to their users with low latency and hig data transfer speeds. 

A VPC NAT gateway will allow internet access to the resources in the private cloud, should the database require an patch. The VPC Endpoint will securely connect the VPC to the AWS services without the need for internet traffic, providing increased security and reduced latency.

![image](https://github.com/dbriones49/Cloud--Three-Tiered-Architecture/assets/143753667/c18f7a8f-e2c8-44f5-87e6-75de10633f70)

