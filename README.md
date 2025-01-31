#Lab 4
Group members:
  - Min Seuk Kim
  - Juan Antony Tarigan

* Instsructions on general set up:
  - Install Terraform
    - Command to identify the hashicorp developers who maintain the repo
      ```sh
      wget -O - https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
      ```
    - Add repo to list of package repositories
      ```sh
      echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
      ```
    - Update and install Terraform
      ```sh
      sudo apt update && sudo apt install terraform
      ```
  - Create configuration files
    - cloud-config.yaml : To define necessary cloud initialization settings
      - Settings includes:
          - user name
          - shell type
          - permission setting for sudo command
          - ssh key
          - packages like nginx and nmap

    - main.tf : To define Terraform resources and configurations for infrastructure deployment

* Command used to create SSH key pair: 
-> ssh-keygen -t rsa -b 4096 -f ~/.ssh/my_terraform_key -N ""

* Commands used for configuration:
  - terraform fmt
  - terraform init
  - terraform plan
  - terraform apply
  - aws configure

* Connect to the EC2 using the users defined in the cloud-config.yaml
  -> ssh -i ~/.ssh/id_rsa <user>@<ipaddress> or <@ec2-52-40-15-90.us-west-2.compute.amazonaws.com>
