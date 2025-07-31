# Terraform Azure Virtual Machine Infrastructure

This project provisions a complete Azure infrastructure using Terraform, including:

- Azure Resource Group
- Virtual Network & Subnet
- Network Security Group (NSG) and rules
- Public IP and Network Interface
- Ubuntu Linux Virtual Machine
- Cloud-init for VM configuration via `customdata.tpl`

---

## Project Structure
```bash
.
├── main.tf              # Main Terraform config
├── customdata.tpl       # cloud-init for provisioning
├── .gitignore
└── README.md
```

##  Getting Started

### Prerequisites

- Terraform v1.4+
- Azure CLI logged in (`az login`)
- SSH key pair generated (saved as `~/.ssh/mtcazurekey` and `mtcazurekey.pub`)

### Usage

```bash
terraform fmt                 # Format code
terraform validate            # Check for syntax errors
terraform init                # Initialize the directory
terraform plan                # Preview the changes
terraform apply -auto-approve # Apply changes
```

## Screenshot
Terraform output after applying the configuration on Azure
![Terraform Output showing Azure resources](./screenshots/terraform-output.png)

## Planned Enhancements (Roadmap)
- [] 🔧 Integrate Ansible to configure Apache and harden the VM
- [] 🔒 Secure credentials using Azure Key Vault
- [] 📊 Enable Azure Monitor and Log Analytics
- [] 🛡️ Harden VM with UFW, Fail2Ban, and best security practices
- [] 🔁 Automate with GitHub Actions CI/CD
- [] 📁 Use Terraform modules to organize infrastructure



## Author
GitHub Profile: [**Nm-mutua**](https://github.com/Nm-mutua)

## Credits   
This project is inspired by the [freeCodeCamp Terraform on Azure tutorial](https://www.youtube.com/watch?v=V53AHWun17s)


  
