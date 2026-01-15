## create a bucket

```sh
aws s3 mb s3://cors-hari-0410
```

## change block public access

```sh
aws s3api put-public-access-block `
--bucket cors-hari-0410 `
--public-access-block-configuration "BlockPublicAcls=true,IgnorePublicAcls=true,BlockPublicPolicy=false,RestrictPublicBuckets=false"
```

## create a bucket policy

aws s3api put-bucket-policy --bucket cors-hari-0410 --policy file://bucket-policy.json

## Turn on static website hosting

```sh
aws s3api put-bucket-website --bucket cors-hari-0410 --website-configuration file://website.json
```

## upload our index.html file and include a resource that would be cross-origin

aws s3 cp index.html s3://cors-hari-0410

## view the website

http://cors-hari-0410.s3-website.ap-south-1.amazonaws.com

## Creating APigateway end point to test cors

Invoke-WebRequest `
  -Uri "https://wo05mvw6je.execute-api.ap-south-1.amazonaws.com/prod/hello" `
  -Method POST `
  -Headers @{ "Content-Type" = "application/json" } `
  -Body '{"message":"Hello from PowerShell"}'


