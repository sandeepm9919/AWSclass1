<ins>**Step-by-Step flow from AWS S3 to AWS Glue using IAM roles and policies:**



![](Media/aws_project_image.jpeg)


**FLOW:**


* Initially we need data files (e.g., CSV, JSON) to upload into the S3 bucket.

 **1) Setup AWS S3 Bucket:** First, ensure we need an AWS S3 bucket where our data files is stored. If we don't have one, we need to create it in the AWS Management Console.

 **2) Upload Data files to S3:** Upload our data files (e.g., CSV, JSON) into the S3 bucket. Make sure the data is organized in a way that makes sense for querying.

 **3) Create an IAM Role:**

* Go to the IAM console.
* Click on "Roles" from the left-hand menu.
* Click on "Create role".
* Choose the service that will use this role (AWS Glue).
* Attach policies that grant necessary permissions. At minimum, attach the "AWSGlueServiceRole" policy to allow Glue to access resources.
* Review and name our role, then click "Create role" and finally role created successfully.

**4) Attach Additional Policies:**

* Go to the Create policy and click JSON and remove the existing code and add the new JSON format which includes S3 bucket ARN in the place of Resource, then click next and then name our policy and create the policy.
* Now again come to the roles and click the specific role which we created in point 3, and then click add permissions then attach policies and search for  policy name which we created before and 



