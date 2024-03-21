# s3bucket_and_EC2 instance
1. The following steps define the execution process:
2. Step 1: Create an EC2 instance and S3 bucket.
3. Step 2: Go to IAM and attach S3 full access to the role and then finally assign this role to the created EC2 instance.
4. Step 3: SSH and perform the actions to check the connectivity between EC2 instance and S3 bucket, create files and upload them to the S3  bucket and also transfer to EC2 instance.
Commands:
  1. sudo apt update
  2. sudo apt install awscli
  3. aws --version
  4. aws s3 ls
  5. vi/nano your_filename
  6. Upload the file to S3 bucket using the command: aws s3 cp your_filename s3://your_bucket_name/your_target_filename
  7. Verify the files from the S3bucket on AWS Console and CLI.
  8. Upload the files to EC2 instance from S3bucket using the command: aws s3 cp s3://your_bucket_name/your_target_filename your_target_filename
  9. For example:
  10. aws s3 cp index.html s3://mybucket/index.html (REF POINT 6)
  11. aws s3 cp s3://mybucket/index.html htmlfroms3 (REF POINT 8)
These steps make one to successfully launch websites as well using CLI and S3 bucket.
