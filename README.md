# Udacity Cloud DevOps Nanodegree

## Project 3: Give Your Application Auto-Deploy Superpowers

### URLS

- URL01 - https://github.com/codeprefect/udacity-devops-nd-03-autodeploy.git
- URL02 - TODO: deployed application URL (S3 Bucket)
- URL03 - TODO: deployed application URL (CloudFormation)
- URL04 - TODO: backend application URL

### Pictures

Please find the details of my submission for project 3.

#### Figure 1 (Failed due to compile errors)

![Compile error](./docs/screenshots/SCREENSHOT01.png)

#### Figure 2 (Failed unit tests)

![Failed Frontend Test](./docs/screenshots/SCREENSHOT02-1.png)

![Failed Backend Test](./docs/screenshots/SCREENSHOT02-2.png)

#### Figure 3 (Found vulnerabilities)

![Vulnerabilities](./docs/screenshots/SCREENSHOT03.png)

#### Figure 4 (Failed build alert)

![Failed Build Alert](./docs/screenshots/SCREENSHOT04.png)

#### Figure 5 (Failed infra creation)

![Failed infrastructure creation](./docs/screenshots/SCREENSHOT05.png)

#### Figure 6 (Failed smoke test)

![Failed smoke test](./docs/screenshots/SCREENSHOT06.png)

#### Figure 7 (Successful rollback after failed smoke test)

![Rollback after failed smoke test](./docs/screenshots/SCREENSHOT07.png)

#### Figure 8 (Successful promotion to production)

![Successful promotion](./docs/screenshots/SCREENSHOT08.png)

#### Figure 9 (Successful cleanup job)

![Successful cleanup](./docs/screenshots/SCREENSHOT09.png)

#### Figure 10 (Trigger evidence - master only)

![Trigger evidence](./docs/screenshots/SCREENSHOT10.png)

#### Figure 11 (Prometheus - EC2 CPU and Disk Usage)

![Prometheus Dashboard](./docs/screenshots/SCREENSHOT11.png)

#### Figure 12 (Prometheus / AlertManager alert for EC2)

![Prometheus Alerts](./docs/screenshots/SCREENSHOT12.png)

### Deployment Evidences

#### Figure 1 (URL03 Screenshot)

![CloudFormation deployment](./docs/screenshots/URL03_SCREENSHOT.png)

#### Figure 2 (URL04 Screenshot - Healthy backend)

![Backend](./docs/screenshots/URL04_SCREENSHOT.png)

#### Figure 3 (URL05 Screenshot - Prometheus Server)

![Prometheus](./docs/screenshots/URL05_SCREENSHOT.png)

### How to reproduce

#### Create/Update required network infrastructure

```[bash]
./network/network-script-create.sh stack-name aws-region
# feel free to change the region to your own preferred region e.g
# ./network/network-script-create.sh udagram-network us-east-1
```

```[bash]
./network/network-script-update.sh stack-name aws-region, please use the same region used in create
# feel free to change the region to your own preferred region e.g
# ./network/network-script-update.sh udagram-network us-east-1
```

#### Create/Update application servers and other resources

```[bash]
./app-script-create.sh stack-name aws-region
# feel free to change the region to your own preferred region e.g
# ./app-script-create.sh udagram-clone us-east-1
```

```[bash]
./app-script-update.sh stack-name aws-region, please use the same region used in create
# feel free to change the region to your own preferred region e.g
# ./app-script-update.sh udagram-clone us-east-1
```

#### Optional - Create/Update jump servers

```[bash]
./jump-server/jump-script-create.sh stack-name aws-region
# feel free to change the region to your own preferred region e.g
# ./jump-server/jump-script-create.sh udagram-clone us-east-1
```

```[bash]
./jump-server/jump-script-update.sh stack-name aws-region, please use the same region used in create
# feel free to change the region to your own preferred region e.g
# ./jump-server/jump-script-update.sh udagram-clone us-east-1
```

Thank you.
