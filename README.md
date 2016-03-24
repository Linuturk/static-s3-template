
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
 * **TTL** - The number of seconds CloudFront should cache content.
  * Default: `86400`

## Mappings

 * **RegionMap**:
  * `(u'us-east-1', {u'websiteendpoint': u's3-website-us-east-1.amazonaws.com', u'S3hostedzoneID': u'Z3AQBSTGFYJSTF'})`
  * `(u'ap-northeast-1', {u'websiteendpoint': u's3-website-ap-northeast-1.amazonaws.com', u'S3hostedzoneID': u'Z2M4EHUR26P7ZW'})`
  * `(u'sa-east-1', {u'websiteendpoint': u's3-website-sa-east-1.amazonaws.com', u'S3hostedzoneID': u'Z31GFT0UA1I2HV'})`
  * `(u'ap-southeast-1', {u'websiteendpoint': u's3-website-ap-southeast-1.amazonaws.com', u'S3hostedzoneID': u'Z3O0J2DXBE1FTB'})`
  * `(u'ap-southeast-2', {u'websiteendpoint': u's3-website-ap-southeast-2.amazonaws.com', u'S3hostedzoneID': u'Z1WCIGYICN2BYD'})`
  * `(u'us-west-2', {u'websiteendpoint': u's3-website-us-west-2.amazonaws.com', u'S3hostedzoneID': u'Z3BJ6K6RIION7M'})`
  * `(u'us-west-1', {u'websiteendpoint': u's3-website-us-west-1.amazonaws.com', u'S3hostedzoneID': u'Z2F56UZL2M1ACD'})`
  * `(u'eu-west-1', {u'websiteendpoint': u's3-website-eu-west-1.amazonaws.com', u'S3hostedzoneID': u'Z1BKCTXD74EZPE'})`

## Resources

 * **BucketPolicy** - `AWS::S3::BucketPolicy`
 * **CloudFront** - `AWS::CloudFront::Distribution`
 * **LogBucket** - `AWS::S3::Bucket`
 * **RootBucket** - `AWS::S3::Bucket`
 * **wwwBucket** - `AWS::S3::Bucket`

## Outputs

 * **CloudFrontURL** - `{u'Fn::GetAtt': [u'CloudFront', u'DomainName']}`
