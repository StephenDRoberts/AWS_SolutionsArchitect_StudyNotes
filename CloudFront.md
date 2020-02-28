# CloudFront

#### Signed URLs & Signed Cookies

CloudFront Signed URLs and signed cookies provide the same basic functionality:
- they allow you to control who can access your content.

*When to use Signed URLs*
* You want to use an RTMP distribution. Signed cookies aren't supported for RTMP distributions (Real Time Messaging Protocol - used for media streaming).
* You want to restrcit access to individual files, for example, an installation download for your application.
* You want to restrict access to individual files, for example, an installation download for your application.

*When to use Signed Cookies*
* You want to provide access to multiple restricted files, for example, all of the files for a video in HLS format or all of the files in the subscribers' are of a website.
* You don't want to change your current URLs.

#### Lambda@Edge

Lambda@Edge is a feature of Amazon CloudFront that lets you run code closer to users of your application, which improves performance and reduces latency.

Lambda@Edge lets you run Lambda functions to customise the content that CloudFront delivers, executing the functions in AWS locations closer to the viewer. The functions run in response to CloudFront events, without provisioning or managing servers. You can use Lambda functions to change CloudFront requests and responses at the following points:
* After CloudFront receives a request from a viewer (viewer request)
* Before Cloudfront forwards the request to the origin (origin request)
* After CloudFront receives the response from the origin (origin response)
* Before CloudFront forwards the response to the viewer (viewer response)
