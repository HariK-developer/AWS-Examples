## Create a new s3 bucket 
aws s3 mb s3://checksums-example-hari-0410

## create a file that will do a checksum on 
echo "Hello Mars" > myfile.txt

## Get a checksum of a file md5 
md5sum myfile.txt
# 68b329da9893e34099c7d8ad5cb9c940

## upload our file to s3
