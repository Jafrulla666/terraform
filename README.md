# Terraform Usage Commands

# terraform init
when first starting to use Terraform, you need to run terraform init to tell Terraform to scan the code, figure out what providers you’re using, 
and download the code for them. By default, the provider code will be downloaded into a .terraform folder, which is Terraform’s scratch directory
(you may want to add it to .gitignore). You’ll see a few other uses for the init command and .terraform folder later on. 
For now, just be aware that you need to run init any time you start with new Terraform code, and that it’s safe to run init multiple times (the command is idempotent).

# terraform plan
 The plan command lets you see what Terraform will do before actually doing it. 
 This is a great way to sanity check your changes before unleashing them onto the world.
 The output of the plan command is a little like the output of the diff command: 
 resources with a plus sign (+) are going to be created, resources with a minus sign (-) are going to be deleted, 
 and resources with a tilde sign (~) are going to be modified in-place. In the output above, you can see that Terraform is planning on creating a single EC2 Instance and nothing else, which is exactly what we want

# terraform apply
 You’ll notice that the apply command shows you the same plan output and asks you to confirm if you actually want to proceed with this plan.
 So while plan is available as a separate command, it’s mainly useful for quick sanity checks and during code reviews, 
 and most of the time you’ll run apply directly and review the plan output it shows you.
 
 # terraform destroy
   When you’re done experimenting with Terraform, it’s a good idea to remove all the resources you created so AWS doesn’t charge you for them.
   Since Terraform keeps track of what resources you created, cleanup is simple. All you need to do is run the destroy command:
