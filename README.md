
## Description

Creates the necessary resources to host a static site in S3.

## Parameters

 * **DomainName** - The root domain name of your site. (example.com)
 * **Error** - The error document for your site.
  * Default: `error.html`
 * **Index** - The index document for your site.
  * Default: `index.html`
 * **LogExpiration** - The number of days to retain access logs.
  * Default: `30`

## Resources

 * **CloudFront** - `AWS::CloudFront::Distribution`
 * **LogBucket** - `AWS::S3::Bucket`
 * **RootBucket** - `AWS::S3::Bucket`
 * **wwwBucket** - `AWS::S3::Bucket`

## Outputs

 * **CloudFrontURL** - `{u'Fn::GetAtt': [u'CloudFront', u'DomainName']}`
