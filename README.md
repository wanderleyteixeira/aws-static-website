# AWS Static Website - Infrastructure as Code
Infrastructure for static website hosted with S3 and CloudFront with a custom domain.

## Diagram
![alt CloudFormation](cloudformation-diagram.png)

## Resources provisioned

* S3 bucket for web site content
* Access logs written to logs bucket
* ACM Certificate for SSL
* CloudFront distributions for website https access
* Route 53 hosted zone with DNS entries

Note: For the `www` to zone apex redirection, we use Route 53 ALIAS feature in `A` record.

## ToDo

Fix default root object (index.html) in subdirectories using [Lambda@Edge](https://aws.amazon.com/blogs/compute/implementing-default-directory-indexes-in-amazon-s3-backed-amazon-cloudfront-origins-using-lambdaedge/).

### References

Many thanks to [alestic](https://github.com/alestic/aws-git-backed-static-website) and [sjevs](https://github.com/sjevs/cloudformation-s3-static-website-with-cloudfront-and-route-53)
