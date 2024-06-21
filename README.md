# Tutorial - AWS Batch Job with Bitcoin app
Steps to configure the AWS batch job for the python bitcoin app

## AWS Batch - Things to understand
* Create Compute Environment
  * `Environment Configuration` - Fargate env, Name of the CE, ServiceRole (BatchServiceRolePolicy)
  * `Instance Configuration` - maximum vCPUs
  * `Network Configuration` - VPC, Subnet, SGs
 
* Create Job Queues
  * `Orchestration type` - Fargate
  * Name of queue
  * Priority
  * Select the above created CE
  * Create Queue
 
* Create Job Definitions
* ![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/300fd1f2-1542-4da7-bc8e-33c3d63b8ca7)




# BitCoin App
* This app is used to get the bitcoin price which is written using flask. 
* Create a role or configure the aws credentials to put the output to DynamoDB table

### Create Docker image
* docker build -t bitcoin .

### Run Docker Container
* docker run --name bitcoin-app-cont bitcoin

#### Sample Output
```
[ec2-user@ip-172-31-38-243 bitcoin_app]$ docker run --name bitcoin-app-cont bitcoin
Item {'amount': {'S': '64189.985'}, 'base': {'S': 'BTC'}, 'currency': {'S': 'USD'}, 'timestamp': {'S': '2024-06-21T20:35:47.560652+05:30'}, 'uuid': {'S': 'eb6c42e0-b326-43cf-9b4b-a2570279522f'}} added to DynamoDB table bitcoin_price_storer.
Data transfer complete.
```
