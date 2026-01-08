## create a bucket
aws s3 mb s3://hari-fun-hk-0410

## create file
echo "Hello world" > hello.txt

## copy object
aws s3 cp hello.txt s3://hari-fun-hk-0410

## change storage class
aws s3 cp hello.txt s3://hari-fun-hk-0410 --storage-class STANDARD_IA

## cleanup
aws s3 rm s3://hari-fun-hk-0410/hello.txt
aws s3 rb s3://hari-fun-hk-0410