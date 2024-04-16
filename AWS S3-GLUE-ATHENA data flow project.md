<ins>**Step-by-Step flow from AWS S3 - AWS Glue - AWS ATHENA using IAM roles and policies:**




![](Media/DATA123.png)

**ENTIRE PIPELINE FLOW:**
* Initially we need data files (e.g., CSV, JSON) to upload into the S3 bucket.

 **1) Setup AWS S3 Bucket:** First, ensure we need an AWS S3 bucket where our data files is stored. If we don't have one, we need to create it in the AWS Management Console. 
 
 
 **2) Upload Data files to S3:** Upload our two data files (e.g., CSV, JSON) into the S3 bucket like we created two separate folders and we inserted one file in one folder.

 ![](Media/BUCKET1.png)


 **3) Updating an IAM Role:**
* Go to the IAM console.
* Click on "Roles" from the left-hand menu.
* Click on "Create role".
* Choose the service that will use this role (AWS Glue).
* Attach policies that grant necessary permissions. At minimum, attach the "AWSGlueServiceRole", "AmazonS3FullAccess" policy to allow Glue to access resources.
* Review and name our role, then click "Create role" and finally role created successfully.

  **4) Attach Additional Policies:**

* Go to the Create policy and click JSON and remove the existing code and add the new JSON format which includes S3 bucket ARN in the place of Resource, then click next and then name our policy and create the policy.
* Now again come to the roles and click the specific role which we created in point 3, and then click add permissions then attach policies and search for  policy name which we created before(if we forget exact names then we search for customer managed  and we can give that names) and add permissions.


**5) Create a Glue Crawler:** 
* Go to the AWS Glue console and create a two new crawlers.
* Configure the two crawlers to point to the S3 bucket where our data is stored.
* Specify the IAM role we created earlier to allow Glue to access the S3 bucket.
* The crawler will automatically infer the schema of our data and create metadata tables in the Glue Data Catalog.

**6)Run the Both Glue Crawlers:** 
* Once the crawler is configured, we run the crawlers.
*  The crawler will scan the data in the S3 bucket, infer its schema, and create or update the metadata tables in the Glue Data Catalog.

**7)Setup Glue Studio:**
* Now, the entire ETL pipeline we create here and we will take the data from the source(s3) and do necessary transformations as per the requirement and finally we will send  the required data to the target(destinations) S3.

![](Media/GLUE1.png)
Above is the place where we do necessary transformations as per the company requirement and we will set up all the target data tables and also we give parquet format to the destination folders.





















