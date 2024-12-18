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
It's true that bucket policies make it really easy to control access for an entire bucket (e.g. making the entire bucket and everything inside public), but ACLs are the way to go if you want to manage access for each object in your bucket individually.

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
```
2) Upload these files into your bucket (right click on each link, and select Save link as index.html and a zip file
```
```
3) Unzip the zip file you've downloaded.
```
```
4) Return to the Amazon S3 console with your bucket page open. Choose the Objects tab.
4.1) Choose Upload.
4.2) Choose Add files.
4.3) Choose index.html.
4.4) Choose Add folder.
4.5) Choose the unzipped folder - NOT the zip file itself!
4.6) You might get a popup that tells you that all files in that folder will be uploaded.
4.7) Choose Upload.
S3 will get to work right away!
```
```
5) Choose Close when you see the green Upload succeeded banner.
```

# Configure a static website on Amazon S3

```
1) Configure your S3 bucket for static website hosting
```
```
2) Visit your public website link.
```

#What does website hosting mean?
Website hosting is what makes your website public on the internet.

Even if you perfect an HTML file, no one else can see it when it's stored as a local file on your computer! Website hosting = storing your HTML file (and the other files for your website) on a web server, so it's accessible online.

By configuring your S3 bucket for hosting, we're telling this bucket: "please create a URL that will take anyone to a page that displays the HTML file I just uploaded."
```
3) Make sure you're back in your bucket's page. If you're not sure, choose Buckets on the left hand side navigation bar, and then choose the bucket you created for this project.
```
```
4) Choose the Properties tab.
```
```
5) Scroll allllllllll the way down to the Static website hosting panel.
```
```
6) Configure the following settings:
6.1) Static web hosting: Choose Enable.
6.2) Hosting type: Choose Host a static website.
6.3) Index document: Enter index.html
```

```
7) Choose Save changes.
```
