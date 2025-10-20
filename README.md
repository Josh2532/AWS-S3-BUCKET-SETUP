# AWS-S3-BUCKET-SETUP
Setting up a simple storage service bucket ( AMAZON S3 )

This project showed how i configured my amazon  s3 bucket for public access 


1.login your aws console and search for s3 

2. clicked on "create  bucket " and named my bucket "josh25-s3-bucket "
 
3. Turned off "block public access" so as to make our object publicly accessible
  
4. uploaded my file (`inventory-springfield`)
 
5. After creating my S3 bucket and uploading a file i added a JSON policy to make it publicly accessible from anywhere in the world on your browser by clicking on the "permissions tab"  and also click on "Edit bucket policy" to input the Json policy  .




{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Sid": "PublicReadAccess",
			"Effect": "Allow",
			"Principal": "*",
			"Action": "s3:GetObject",
			"Resource": "arn:aws:s3:::josh25-s3-bucket/*"
		}
	]
}
