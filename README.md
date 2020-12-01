# Exploring Packer

### Purpose
- Project explores creation of amazon machine images using packer tool.

### Requirements
- [ ] Packer Executable (path established)
- [ ] AWS account with permission to build ami and launch with EC2
- [ ] AWS Cli deploying image from cmdln/terminal

### Implementation (Create AMI)
+ Example 1
    - `cd ami`
    - `packer validate ami/ubuntu_basic.json` then `packer build ami/ubuntu_basic.json`
+ Example 2
    - Export private AWS credentials in terminal
    - - `cd ami`
    - `packer validate ubuntu_script.json` then `packer build ubuntu_script.json`

### Implementation (Create Instance)
- [ ] AWS Cli: `aws ec2 run-instances --image-id <ami_output_id> --count 1 --instance-type <instance_type> --key-name <desired_keypair> --security-group-ids <security_group)id>--subnet-id <subnet_id>`
- [ ] AWS Console: launch instance using packer ami-id output

![Console](img/ec2_launch_screen.jpeg)

### Documentation
- [Packer Tutorial](https://learn.hashicorp.com/tutorials/packer/getting-started-build-image)
