---
title: "Mastering Day 4 of Terraform Basics"
seoTitle: "Day 4: Terraform Basics Mastery"
seoDescription: "Learn essential Terraform lifecycle commands to efficiently manage infrastructure: initialize, plan, apply, destroy, and maintain configurations"
datePublished: Sat Sep 14 2024 12:25:20 GMT+0000 (Coordinated Universal Time)
cuid: cm124eip5000s09mbahw9f5iq
slug: mastering-day-4-of-terraform-basics
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1726159854938/a0324b1f-e65b-484a-ba78-82bd6f29c4bf.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1726159904171/8bb31e9c-481e-475a-8310-5874adc9dd0e.png
tags: cloudformation, cloud, aws, developer, cloud-computing, devops, terraform, aws-lambda, cloud-native, devops-articles, terraform-state, terraform-cloud, devops-trends, devops-journey, devopscommunity

---

Terraform provides several lifecycle commands to manage infrastructure in a declarative manner. These commands allow you to initialize, plan, apply, and destroy infrastructure, as well as manage configurations and states. Below is a detailed breakdown of Terraform lifecycle commands with descriptions, examples, and tips.

---

## Terraform Lifecycle Commands: A Detailed Guide

### 1\. `terraform init` - Initialization

`terraform init` is the first command to run when working with a new or existing Terraform configuration. It initializes the directory, downloads provider plugins, and sets up the backend where Terraform stores its state files.

#### Purpose:

* Download the provider plugins (e.g., AWS, Azure).
    
* Initialize the working directory.
    
* Set up the backend for storing state.
    

#### Syntax:

```plaintext
terraform init [options]
```

#### Example:

```plaintext
terraform init
```

#### Key Options:

* `-input=false`: Disables interactive prompts.
    
* `-backend-config`: Override backend configuration settings.
    

#### Explanation:

When `terraform init` is run, Terraform:

* Checks the configuration file for required providers.
    
* Downloads those provider plugins to `.terraform/plugins`.
    
* Configures the backend (e.g., S3, local storage) to store the Terraform state.
    

#### Tips:

* You only need to run `init` once when setting up the working directory or after modifying the backend configuration.
    
* Running `init` does not make changes to infrastructure, only to the local configuration.
    

---

### 2\. `terraform plan` - Planning

`terraform plan` is used to preview the actions that Terraform will take to modify infrastructure. It compares the current state of infrastructure with the desired state defined in the configuration files and generates an execution plan.

#### Purpose:

* Preview the changes before applying them.
    
* Verify if the desired infrastructure changes are correct.
    

#### Syntax:

```plaintext
terraform plan [options]
```

#### Example:

```plaintext
terraform plan
```

#### Key Options:

* `-out=planfile`: Saves the generated plan to a file to use with `apply`.
    
* `-var 'key=value'`: Passes variables from the command line.
    
* `-target=resource`: Focuses the plan on a specific resource or module.
    

#### Explanation:

Running `terraform plan` allows you to see what Terraform will do (create, update, or destroy) without actually applying any changes. This gives you the opportunity to review and make sure the plan aligns with your goals.

#### Output:

The output shows:

* **Add**: Resources that will be created.
    
* **Change**: Resources that will be updated.
    
* **Destroy**: Resources that will be deleted.
    

#### Tips:

* Use the **\-out** option to save the plan to a file if you intend to apply it later. This ensures the same plan is applied.
    
* Always run `terraform plan` before applying changes to avoid unexpected modifications.
    

---

### 3\. `terraform apply` - Applying Changes

`terraform apply` is the command that actually provisions, updates, or destroys infrastructure. It takes the desired state from the configuration files and applies it to the real-world infrastructure.

#### Purpose:

* Create, modify, or destroy infrastructure based on the execution plan.
    

#### Syntax:

```plaintext
terraform apply [options] [planfile]
```

#### Example:

```plaintext
terraform apply
```

#### Key Options:

* `-auto-approve`: Skips interactive approval of the plan before applying.
    
* `-var 'key=value'`: Passes variables from the command line.
    

#### Explanation:

Running `terraform apply` applies the actions described in the plan to real infrastructure. If no saved plan file is provided, Terraform will create a new plan before applying it.

#### Output:

After applying, Terraform will output the list of resources that were created, modified, or destroyed, as well as their corresponding identifiers (like instance IDs).

#### Tips:

* Use the `-auto-approve` option in automation pipelines to skip manual approval.
    
* If you saved the plan from the `plan` command using `-out=planfile`, pass that plan file to `apply` to ensure exactly those changes are applied:
    
    ```plaintext
    terraform apply planfile
    ```
    

---

### 4\. `terraform destroy` - Destroying Resources

`terraform destroy` is the opposite of `apply`. It is used to remove infrastructure managed by Terraform. This command is often used during teardown phases in development environments.

#### Purpose:

* Destroy or tear down infrastructure.
    

#### Syntax:

```plaintext
terraform destroy [options]
```

#### Example:

```plaintext
terraform destroy
```

#### Key Options:

* `-auto-approve`: Skips interactive approval for destruction.
    
* `-target=resource`: Destroy a specific resource or module.
    

#### Explanation:

`terraform destroy` compares the current state of the infrastructure to the configuration and destroys all resources managed by Terraform. By default, it asks for confirmation before proceeding.

#### Tips:

* Use `-auto-approve` to skip the confirmation prompt.
    
* Be cautious when using `destroy` in a production environment, as it will remove all resources managed by Terraform.
    

---

### 5\. `terraform fmt` - Formatting Code

`terraform fmt` formats Terraform configuration files (.tf) to ensure they follow a standard style.

#### Purpose:

* Format configuration files to improve readability.
    

#### Syntax:

```plaintext
terraform fmt [options] [path]
```

#### Example:

```plaintext
terraform fmt
```

#### Key Options:

* `-recursive`: Formats files in all subdirectories.
    

#### Explanation:

Running `terraform fmt` ensures that all configuration files conform to the standard formatting style for Terraform, which includes indentation, spacing, and alignment of arguments.

#### Tips:

* Run `terraform fmt` regularly to keep your configuration files clean and readable.
    

---

### 6\. `terraform validate` - Validating Configurations

`terraform validate` checks whether the Terraform configuration files are syntactically valid and internally consistent. This is useful for catching errors early in the development process.

#### Purpose:

* Validate the configuration files before applying changes.
    

#### Syntax:

```plaintext
terraform validate [options] [path]
```

#### Example:

```plaintext
terraform validate
```

#### Explanation:

`terraform validate` checks the syntax and consistency of the configuration files but does not validate if resources are correctly configured in the cloud provider.

#### Tips:

* Run `terraform validate` before planning or applying to catch any syntax errors early.
    
* It doesn’t access external systems, so it is fast and safe to run at any time.
    

---

### Conclusion

Terraform lifecycle commands are essential to managing the full infrastructure provisioning and management cycle. Commands like `init`, `plan`, `apply`, and `destroy` cover the basic infrastructure lifecycle, while others, like `fmt`, `validate` help maintain code quality and extract useful information.

Understanding these commands is crucial for effectively working with Terraform and ensuring a smooth workflow when managing your infrastructure as code.