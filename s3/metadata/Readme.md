
## create a bucket

aws s3 mb s3://metadata-fun-ab-0410

## create a new file

echo "Hello Mars" > hello.txt

## upload file with metadata

aws s3api put-object --bucket metadata-fun-ab-0410 --key hello.txt --body hello.txt --metadata Planet=Mars

## Get Metadata through get object

aws s3api head-object --bucket metadata-fun-ab-0410 --key hello.txt