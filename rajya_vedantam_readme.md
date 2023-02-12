# Maxwell Health / Sun Life Take Home Exercise   

## Open Ports needed for running this application

firewall-cmd --permanent --add-port=41390/tcp
firewall-cmd --permanent --add-port=41391/tcp
firewall-cmd --reload


## Unzip and Run App

cd /home
unzip Node_React_APP.zip
cd Node_React_APP
cd client
npm run build

cd server/
npm start

## Test from the browser using HTTP
 http://<ipaddress>:41390 

## Test from the browser using HTTPS
 https://<ipaddress>:41391



## curl commands

- amazon-status:
    curl http://10.91.170.100:41390/v1/amazon-status
    curl -k https://10.91.170.100:41391/v1/amazon-status
    output:
    '''
    {"url":"https://amazon.com","statusCode":200,"duration":639,"date":1676232064000}                 
    '''
- google-status:
    curl http://10.91.170.100:41390/v1/google-status
    curl -k https://10.91.170.100:41391/v1/google-status
    output:
    '''
    {"url":"https://google.com","statusCode":200,"duration":139,"date":1676232201000}
    '''
- all-status:

    curl http://10.91.170.100:41390/v1/all-status
    curl -k https://10.91.170.100:41391/v1/all-status
    output:
    '''
    [{"url":"https://amazon.com","statusCode":200,"duration":527,"date":1676232229000},{"url":"https://google.com","statusCode":200,"duration":137,"date":1676232229000}]        
    '''