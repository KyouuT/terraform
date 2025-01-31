#Lab 4
Group members:
  - Min Seuk Kim
  - Juan Antony Tarigan

* Command used to create SSH key pair: 
-> ssh-keygen -t rsa -b 4096 -f ~/.ssh/my_terraform_key -N ""

* Commands used for configuration:
  - terraform fmt
  - terraform init
  - terraform plan
  - terraform apply
  - aws configure

* Connect to the EC2 using the users defined in the cloud-config.yaml
  -> ssh -i ~/.ssh/id_rsa <user>@<ipaddress
