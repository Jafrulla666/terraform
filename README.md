# Terraform Usage Commands

# terraform init
            when first starting to use Terraform, you need to run terraform init to tell Terraform to scan the code, figure out what providers you’re using, and download the code for them. By default, the provider code will be downloaded into a .terraform folder, which is Terraform’s scratch directory (you may want to add it to .gitignore). You’ll see a few other uses for the init command and .terraform folder later on. For now, just be aware that you need to run init any time you start with new Terraform code, and that it’s safe to run init multiple times (the command is idempotent).
