# Terraform-Static-Website
This Terraform code creates a static website hosted on AWS S3. It sets up an S3 bucket, configures the bucket as a static website, and uploads the necessary files to serve the website.

Prerequisites
Before running this Terraform code, you need to have the following prerequisites:

AWS Account: You must have an AWS account with appropriate credentials to create resources like S3 buckets.
AWS CLI: The AWS Command Line Interface (CLI) must be installed and configured with the necessary access credentials.
Getting Started
To create the static website, follow these steps:

Clone the repository containing the Terraform code.
Open a terminal or command prompt and navigate to the directory containing the Terraform code.
Terraform Configuration
The Terraform configuration file main.tf includes the necessary code to create the resources. It uses the AWS provider and specifies the required version.

Variables
The Terraform variables are defined in the variables.tf file. The default value for the bucketname variable is set to "myterraformprojectwebsite2023nickmarch", but you can update it with your desired bucket name.

S3 Bucket Creation
The Terraform code creates an S3 bucket with the specified bucket name.

S3 Bucket Ownership Controls
The Terraform code applies ownership controls to the S3 bucket, ensuring that objects uploaded to the bucket are owned by the bucket owner.

S3 Bucket Public Access Block
The Terraform code sets up public access block configurations to prevent public access to the bucket.

Uploading Website Files
The Terraform code uploads the index.html, error.html, and me.jpg files to the S3 bucket. The index.html and error.html files contain the content for the website and error page, respectively.

S3 Bucket Website Configuration
The Terraform code configures the S3 bucket to serve as a static website, using index.html as the default document and error.html as the error document.

Output
After running Terraform successfully, you will see an output with the S3 bucket's website endpoint.

Website Content
The website content is contained within the index.html file, which showcases a basic portfolio layout with placeholder project descriptions. The error.html file is used as the error page to handle any unexpected issues.

You can update the index.html and error.html files with your content to customize the website as needed.

Deploy the Website
To deploy your static website, follow these steps:

Ensure you have the necessary AWS credentials configured on your system.
Run terraform init to initialize the Terraform configuration.
Run terraform apply and confirm the creation of resources.
After the deployment is complete, you can access your website using the website endpoint provided in the output.
Remember to destroy the resources when they are no longer needed by running terraform destroy to avoid incurring unnecessary costs.

By following these steps, you can create and deploy your static website on AWS S3 using Terraform.
