Terraform module to provision an EC2 instance that is running Apache.

Not intended for prod use just showcasing how to create a public module in Terraform registry.

```hcl
module "apache" {
    source =".//terraform-aws-apache-example"
    vpc_id = "vpc-00000"
    my_ip_with_cidr = "MY-OWN-IP-ADDRESS/32"
    public_key = "ssh-rsa AAAAA"
    instance_type="t2.micro"
    server_name="Apache Example Server"
}
```