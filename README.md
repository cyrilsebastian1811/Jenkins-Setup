# infrastructure

To create vpc and ec2 instance run command 

AWS_PROFILE=prod ansible-playbook -i development  aws_vpc_ec2_setup.yml  --extra-var "key_pair=<ec2_key_pair> route53_zone_name=<domain_name> route53_record_name=<jenkins.domain_name> letsencrypt_email=<your_email_id> domain_name=<jenkins.domain_name> staging_cert=false"  -vvv

<!-- AWS_PROFILE=dev ansible-playbook -i development aws_vpc_ec2_setup.yml --extra-var "key_pair=csye7374 route53_zone_name=jenkins.dev.cyril-sebastian.com route53_record_name=jenkins.dev.cyril-sebastian.com letsencrypt_email=a@a.com domain_name=jenkins.dev.cyril-sebastian.com staging_cert=true"  -vvv -->

To teardown vpc and ec2 instance run command

AWS_PROFILE=prod ansible-playbook -i development aws_vpc_ec2_teardown.yml --extra-var "key=app value=jenkins"

<!-- AWS_PROFILE=dev ansible-playbook -i development aws_vpc_ec2_teardown.yml --extra-var "key=app value=jenkins" -->

