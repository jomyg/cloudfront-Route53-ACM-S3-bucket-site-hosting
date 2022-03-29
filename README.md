#Setting-Cloudfront-for-s3-as origin

[![Build](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

## Description

Amazon CloudFront is a global content delivery network (CDN) service built for high-speed, low-latency performance, security, and developer ease-of-use. We can set Cloudfront to different origins as Ec2 instance, S3 bucket.
Amazon CloudFront is a content delivery network operated by Amazon Web Services. Content delivery networks provide a globally-distributed network of proxy servers that cache content, such as web videos or other bulky media, more locally to consumers, thus improving access speed for downloading the content.

## Pre-Requests
```
S3 Bucket with static site enabled
ROute 53
ACM - For ssl
CLoudfront with OAI Enabled
```

#### OAI : origin access identity

The request to create a new origin access identity (OAI). An origin access identity is a special CloudFront user that you can associate with Amazon S3 origins, so that you can secure all or just some of your Amazon S3 content.

### Lets go to the deployment:
#### Step 1 Create S3 bucket
```
Create a S3 Bucket with default settings and only enable the static website host.
Upload your site contents to your s3 bucket and save it
```
firefox_DGtdzi0s5Y.png

Step 2 : Create Cloudfront

```
* Select your
```
firefox_qixMhEUp8L.png
















## Conclusion



#### ⚙️ Connect with Me

<p align="center">
<a href="mailto:jomyambattil@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://www.linkedin.com/in/jomygeorge11"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a> 
<a href="https://www.instagram.com/therealjomy"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white"/></a><br />
