![MasterHead](https://cdn.dribbble.com/userupload/7725814/file/original-ad34e5a3d587a8a90b6586de67710225.gif)
<h1 align="center">Hi 👋, I'm Paulo César Nunes from Brazil🇧🇷</h1>

<h3 align="center">DevOps Engineer focused on automation and cloud technologies for efficiency.</h3>
<img align="center" alt="Scripting" width="400" src="https://cdn.dribbble.com/userupload/7725640/file/original-a2b82ab8779ece4c49df3672f7753ccb.gif">

<br />

<h2 align="center">Setup Network in AWS using Terraform (Amazon VPC)</h2>

<br />

#### ➤ [subnet-public-private](https://gitlab.com/pcnuness/iac/terraform/provider-family-aws/provider-aws-vpc)

```bash
module "vpc" {
  #source = "<path>/provider-family-aws/provider-aws-vpc/subnet-public-private"
  #source = "git::https://gitlab.com/pcnuness/iac/terraform/provider-family-aws/provider-aws-vpc.git/modules/subnet-public-private?ref=v0.0.1"

  region      = "us-east-1"
  environment = "production"
  vpc_cidr = {
    range = "172.20.0.0/20"
  }

  num_azs = 2

  create_database_subnet_group = true
  type_database_subnet_group = {
    private = true
    public  = true
  }

  subnet_mask = {
    private = 4
    public  = 4
  }

  subnet_mask_init = {
    public = 2
  }

}
```
</p>

<br />

<h3 align="left">Languages and Tools</h3>

<br />

<h3 align="left">Blogs posts</h3>
<p align="left">
<a href="https://pcnunes.com.br" target="_blank">Paulo César Nunes On Blog </a>
</p>

