
## create our bucket
* aws s3 mb s3://prefixes-fun-ab-0410

## create our folder
* aws s3api put-object --bucket="prefixes-fun-ab-0410" --key="hello/"