# Tutorial - AWS Batch Job with Bitcoin app
Steps to configure the AWS batch job for the python bitcoin app

# BitCoin App
* This app is used to get the bitcoin price which is written using flask. 
* Create a role or configure the aws credentials to put the output to DynamoDB table

## Initial Tests
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


## AWS Batch - Things to understand
### Create Compute Environment
![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/ee466d36-2ca0-46f9-b615-57f28f2409c0)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/3ebd4ae8-aab0-4c14-bd1a-bba99da0aa2f)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/73d5d99b-cf6f-4f3e-997c-5bcf51d31575)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/e4dbb12d-e494-444f-949d-453346c57d46)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/8f3e7db8-2a5e-4fc4-a53b-1203b6442580)

### Create Job Queue
![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/768f6ef4-f959-468a-9252-b81f1f44ba0d)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/976afb1c-6f19-422f-b6f4-debe77b9507c)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/8984b2e2-966a-40ca-b097-c6a8c6fdc73b)

### Create Job Definitions
![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/f46915ff-3cb7-437b-8e43-7a419a4362d6)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/f827e489-1744-47f2-bb6d-00fedfa5d6eb)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/3922d6fa-3b4f-4d7e-9055-a09727548f0e)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/0aacb9b8-5804-4e1b-8e66-8da9e15f5ce3)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/55429d54-49c4-46ed-a158-945dc5601970)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/f3b5faf8-54f1-4307-84d7-5f932a7ef04a)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/90ecc6f9-052d-49f8-9c64-9a3f95e25604)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/2916dfcd-30b7-4de0-a13b-78dc85ee5fbf)


### Create Jobs
![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/e98e8589-836f-42c7-9b26-f7241d5cb8e2)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/d46a137b-57d1-4451-a10b-ac7714f61559)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/bee74b1d-4320-4059-ba7f-7b659f763546)

### Checking LogStream for Output
![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/20ce19d9-cf67-4a04-ae02-755480693002)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/8443f501-b43e-4f47-bdac-1b36e809181e)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/50cbcfa6-8a58-46de-8618-d767944dd0f5)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/c32aeb03-78f4-420b-84e0-1ee4971661b8)

![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/38244958-f5fc-4ca4-b716-87552ce66c9c)

### AWS Role
![image](https://github.com/devopsvish/bitcoin_app/assets/88719789/7a100d47-8d0a-41cd-bc71-45a52561ec68)
