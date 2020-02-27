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

