aws budgets create-budget \
    --account-id $ACCOUNT_ID \
    --budget file://aws/json/budget.json \
    --notifications-with-subscribers file://aws/json/budget-notifications-with-subscribers.json


    aws sns subscribe \
    --topic-arn="arn:aws:sns:eu-west-2:767398126092:billing-alarm"\
    --protocol=email \
    --notification-endpoint=pedropereira_90@outlook.com