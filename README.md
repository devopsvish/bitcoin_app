# BitCoin App
This app is used to get the bitcoin price

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
