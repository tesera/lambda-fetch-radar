# lambda-fetch-radar

AWS Lambda function to fetch radar images periodically from weather.gc.ca. The function should be configured to run daily (at any time), and then will visit weather.gc.ca historical imagery and download one image for each of the last 24 hours. The images will then be pushed to AWS S3 (incomplete at this time).

## Install

1. Create a lambda function through the AWS Console.
2. Configure the lambda function to run daily.
3. Copy `sample.env` to `.env` and set the target bucket name inside.
4. Run the deploy script in this repository: `./deploy.sh`

## Usage

Thats it! The lambda function will now run daily and grab the last 24 URLs. It does not yet actually download the images to AWS S3.
