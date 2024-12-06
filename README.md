# aws-private-link
AWS PrivateLink Connection between two VPCs

1. List Pending Endpoint Connections:
aws ec2 describe-vpc-endpoint-connections --query 'VpcEndpointConnections[?ServiceId==`vpce-svc-0cdddaa9d087a92ee`]'

2. Accept the Endpoint Connection Request:
aws ec2 accept-vpc-endpoint-connections --service-id <service-id> --vpc-endpoint-ids <endpoint-id>
aws ec2 accept-vpc-endpoint-connections --service-id vpce-svc-0bd28207a61a0f6be --vpc-endpoint-ids vpce-0bfc7ec82e7690c62


3. From the command line of your instance, run the command 
‘curl http://ENDPOINT-DNS-NAME’ (make sure you paste the DNS name of the VPC endpoint).
