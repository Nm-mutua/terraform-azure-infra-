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

```
.
├── main.tf                  # Main Terraform configuration
├── variables.tf             # Declares input variables
├── osx.tfvars               # Variable values (used with -var-file)
├── .gitignore               # Files/directories to ignore in Git
├── .terraform.lock.hcl      # Dependency lock file for Terraform
├── terraform-output.png     # Screenshot of Azure portal output
└── README.md                # Project documentation
```

##  Getting Started

### Prerequisites

- Terraform v1.4+
- Azure CLI
- SSH (Cloud-init)
- Ubuntu 20.04 LTS

### Usage

```bash
terraform fmt                 # Format code
terraform validate            # Check for syntax errors
terraform init                # Initialize the directory
terraform plan                # Preview the changes
terraform apply -auto-approve # Apply changes
```

### Post-Deployment Configuration

After successful provisioning with Terraform, the following configuration was performed on the Azure VM (`mtc-vm`):

- ✅ Installed Docker Engine on Ubuntu 20.04 LTS  
- 🔧 Verified installation using: `docker --version`  
- 🐳 Purpose: Prepares the VM for container-based workloads (optional future expansion)
- 📜 Installed via cloud-init script defined in [`customdata.tpl`](./customdata.tpl)

## Screenshot
Terraform output after applying the configuration on Azure
![Terraform Output showing Azure resources](./terraform-output.png)

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

## License
This project is licensed under the [MIT License](./LICENSE).

  
