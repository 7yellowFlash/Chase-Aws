## Create Log Group

'''sh
aws logs create-log-group --log-group-name "/examples/basic/app"
'''

## Set Retention on Log Group 

'''sh
aws logs put-retention-policy --log-group-name "/examples/basic/app" --retention-in-days 1
'''

## Create Log Stream 

'''sh
aws logs create-log-stream --log-group-name "/examples/basic/app" --log-stream-name $(date +%s)
''

## Send Logs to Log Stream 
aws logs put-log-events --log-group-name "/examples/basic/app" --log-stream-name 1720622641 --log-events file://events