Setting-Cloudfront-for-s3-as origin

[![Build](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

## Description

Amazon CloudFront is a global content delivery network (CDN) service built for high-speed, low-latency performance, security, and developer ease-of-use. We can set Cloudfront to different origins as Ec2 instance, S3 bucket.
Amazon CloudFront is a content delivery network operated by Amazon Web Services. Content delivery networks provide a globally-distributed network of proxy servers that cache content, such as web videos or other bulky media, more locally to consumers, thus improving access speed for downloading the content.

<center><img alt="ACM" src="cloudfront.png"> </img></center>

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
<center><img alt="ACM" src="firefox_DGtdzi0s5Y.png"> </img></center>


Step 2 : Create Cloudfront

```
* Select your S3 bucket on cloudfront "orgin domain" 
* On Viewer protocol policy, slect the HTTP to HTTPS Redirect.
* On Settings, you can choose the edge locations
* At Alternate domain name (CNAME), provide a name called like "cloud.jomygeorge.xyz"
* Finaly create a ACM SSL, Associate a certificate from AWS Certificate Manager. The certificate must be in the US East (N. Virginia) Region (us-east-1). For this     you can request on time and add its records to ROute 53 for the verifications. 
* Default root object : index.html in my case
```

<center><img alt="ROute53" src="firefox_qixMhEUp8L.png"> </img></center>
<center><img alt="ROute53" src="firefox_SpNZDUqSni.png"> </img></center>
<center><img alt="ROute53" src="firefox_MS3BBLGeqh.png"> </img></center>
<center><img alt="ACM" src="firefox_BCNf3Jd2Vh.png"> </img></center>

Step 2 : On ROute 53
```
* Create a A record for the subdomain "cloud.jomygeorge.xyz" 
* Then Route traffic to as alias "Alias to cloudfront distrubution" and slect you cloudfront ID
* Create the record now
```
<center><img alt="ROute53" src="firefox_2uPUh59oU0.png"> </img></center>

## Conclusion

In this tutorial we discussed how to set a cloudfront for an S3 origin. The goal is to get you started on using Amazon CloudFront for for high-speed, low-latency performance, security, and developer ease-of-use as it is cheap and easy to do.

<center><img alt="ROute53" src="firefox_TRJyIf9gcN.png"> </img></center>

#### ⚙️ Connect with Me

<p align="center">
<a href="mailto:jomyambattil@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://www.linkedin.com/in/jomygeorge11"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a> 
<a href="https://www.instagram.com/therealjomy"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white"/></a><br />
