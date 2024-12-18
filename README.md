# Host-a-website-on-Amazon-S3


# Steps:

# Create a bucket in Amazon S3 
```
1) Open Amazon S3
```
```
2) Create a storage space for your website files.
```
```
3) Log in to AWS.
```
```
4) In the AWS Management Console, search for S3.
4.1) Select the AWS Region closest to you. You can find this at the top right corner of your AWS Management console, right next to your name!
4.2) Choose Create bucket.
4.3) For Bucket name, enter nextwork-website-project-name
4.4) Make sure to replace name with your name.
```


# Why can't I just keep 'name' in the bucket name?
An S3 bucket name is globally unique. After you create a bucket, no other AWS account in the entire world can use your bucket's name (unless you delete the bucket).

This also means that when you create your bucket, you need to make sure the bucket's name is unique too.



```
5) For Object Ownership, choose ACLs enabled.
```

# what are ACLs (Access Control Lists)?
An ACL = a set of rules that decides who can get access to a resource.

Enabling ACLs in this S3 setup lets you control who can access and do things with the objects (i.e. website files) you upload into your bucket.

With ACLs, different AWS accounts can own and control different files in your bucket.

```
6) Choose Bucket owner preferred.
```

```
7) For Block Public Access settings for this bucket, clear the check box for Block all public access.
7.1) Check the box that says “I acknowledge that the current settings might result in this bucket and the objects within becoming public.”
```
# What is the yellow pop up saying?
A yellow warning banner will pop up when you enable ACLs. This banner tells you that it's simpler to use another tool called bucket policies.

```
8) For Bucket Versioning, choose Enable.
```
```
9) Choose Create bucket.
```

# Upload website content to your bucket
Phew, that's your S3 bucket all created.

Time to get those website's files inside your bucket!
```
1) In the Buckets section, choose the name of your new bucket.
```
```2) 


It's true that bucket policies make it really easy to control access for an entire bucket (e.g. making the entire bucket and everything inside public), but ACLs are the way to go if you want to manage access for each object in your bucket individually.

