# aws-private-link
AWS PrivateLink Connection between two VPCs

1. List Pending Endpoint Connections:
aws ec2 describe-vpc-endpoint-connections --query 'VpcEndpointConnections[?VpcEndpointState==`pendingAcceptance`]'

2. Accept the Endpoint Connection Request:
aws ec2 accept-vpc-endpoint-connections --service-id <service-id> --vpc-endpoint-ids <endpoint-id>

3. From the command line of your instance, run the command 
‘curl http://ENDPOINT-DNS-NAME’ (make sure you paste the DNS name of the VPC endpoint).
