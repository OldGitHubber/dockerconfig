# Docker installation files
There are various versions of the same thing

**docker-az.sh** is for use without terraform. It puts the user in the Docker group

**docker-az-tf.sh** is for use with terraform. It doesn't put the user in the Docker group as this causes Terraform to fail. Terraform will add the user to the Docker group

**docker-az-swap.sh** is for use without Terraform and adds a swap file to the system disk to enable a database to run on a small VM such as B1s

**docker-az-tf-swap.sh** is for use with Terraform and adds a swap file to the system disk to enable a database to run on a small VM such as B1s

**docker-aws.sh** is for use without Terraform and installs Docker on an AWS EC2


You can pull the file onto a vm in a user data config or a Terraform remote provisioner. The following is an example of pulling the Terraform with swap file option:

``` sh
curl https://raw.githubusercontent.com/oldgithubber/dockerconfig/main/docker-az-tf-swap.sh
```