
###  create a bucket and upload resource
```
bucketregion=us-east-1
bucketname=
filename=
```
```
aws s3api create-bucket \
    --bucket $bucketname \
    --region $bucketregion
```
```
aws s3 cp $filename s3://$bucketname/ --region=$bucketregion --recursive
```
```
aws s3api list-objects --bucket=$bucketname --query 'Contents[].Key' --output text
```