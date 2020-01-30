# infrastructure

To create vpc and ec2 instance run command 

ansible-playbook -i development  aws_vpc_ec2_setup.yml  --extra-var "key_pair=<ec2_key_pair> route53_zone_name=<domain_name> route53_record_name=<jenkins.domain_name> letsencrypt_email=<your_email_id> domain_name=<jenkins.domain_name>"  -vvv

To teardown vpc and ec2 instance run command

ansible-playbook -i development aws_vpc_ec2_teardown.yml --extar-var "key=app value=jenkins" -vvv

