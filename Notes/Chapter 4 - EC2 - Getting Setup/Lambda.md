# Lambda



## User comments

### One million lambda functions by [endofcake](https://acloud.guru/named/endofcake)

Some of the assertions are incorrect.

- when a million users hit your API endpoint you will not get one million separate lambda functions. The function instancess will be reused between invocations (with state being preserved within the same function instance - it's really important to remember this). Don't forget that there's a default limit of 1000 concurrent executions too (http://docs.aws.amazon.com/lambda/latest/dg/limits.html)

- lambda doesn't scale instantly, cold executions take a noticeable amount of time (provision a container, download code from S3, verify code, initialise it). It's more noticeable when your lambda is large (for example, written in Java). There are some tricks to keep your lambdas hot to avoid this penalty.

There are also some downsides to using lambda which are not mentioned at all (security implications, limited control over your environment). It's important to realise that it's not a silver bullet.

### Question: Lambda running outside of VPC by [ramya_nataraj](https://acloud.guru/named/ramya_nataraj)

**If lambda runs outside of VPC, I understand that IP addresses of lambda will be dynamically generated within aws. But will the dynamically generated IP fall within the region in which lambda is deployed(us-east-1). If my lambda running outside the VPC is making a third party HTTP call, can I assume that the IP address from which call will be made to the 3rd party be from one of us-east-1 CIDR blocks of IP?**

#### Answered by [pave barakin](https://acloud.guru/named/pavel%20barakin)

> Each region is completely independent, so the answer should be yes.

> It's confirmed by statistical data about IP Address ranges to which Lambda outgoing IP can belong in each region, see CIDR section at http://cloudsnoop.io/aws-lambda-available-rpm-packages-and-modules/

> For more information about AWS IP Address ranges for different regions see http://docs.aws.amazon.com/general/latest/gr/aws-ip-ranges.html

#### Answered by [mfenimore70](https://acloud.guru/named/mfenimore70)

> I wonder what it will do to your IP issue . . . I just received an email announcement from AWS today about Lambda@edge: https://aws.amazon.com/lambda/edge/ A new AWS Lambda feature that lets you run code across global AWS locations without provisioning or managing servers. You just upload your code to AWS Lambda and configure it to be triggered by Amazon CloudFront events. This should be interesting.

### Question: lambda disadvantages by [John Abram Cruz](https://acloud.guru/named/John%20Abram%20Cruz)

**What is the disadvantages of lambda? I know that there is timeout for it so that if its a long running task it could be a problem.**
