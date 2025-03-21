# Usage 
## Copy paste below code and update the config
```
module "helm-app" {
  source      = "./appmodule"
  name        = "terraform-helm-app"
  namespace   = "default"
  values_yaml = <<EOF

replicaCount: 5

image:
  repository: binami/wordpress
  pullPolicy: IfNotPresent
  tag: "latest"


  EOF
}
```
### Run the following commands 
```
terraform init 
terraform apply 
````