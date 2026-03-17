**Installation of Terraform**

The installation of Terraform was carried out on a Windows operating
system as part of setting up a DevOps development environment.

To begin, the latest version of Terraform was downloaded from the
official HashiCorp Terraform website. The appropriate version for the
system architecture (Windows AMD64) was selected and downloaded as a
compressed (.zip) file. After the download, the file was extracted, and
the executable file (terraform.exe) was obtained.

A new directory was created on the local disk (C:\\terraform), and the
extracted executable file was moved into this folder to ensure a
consistent and accessible location.

To enable the system to recognize Terraform commands globally, the
folder path (C:\\terraform) was added to the system is Environment
Variables under the PATH configuration. This step was necessary to allow
Terraform to be executed from any directory within the terminal.

After configuring the PATH, the system was restarted to apply the
changes. However, upon testing the installation using Git Bash, the
command terraform version returned an error indicating that the command
was not recognized.

Further investigation revealed that although Terraform was correctly
installed, Git Bash was not inheriting the Windows system PATH as
expected. This led to a temporary workaround where the full path to the
executable (/c/terraform/terraform.exe) was used to verify that
Terraform was functioning correctly.

To resolve the issue permanently, the PATH was manually updated within
Git Bash by modifying the \~/.bashrc file to include the Terraform
directory with this command:  echo \'export PATH=\$PATH:/c/terraform\'
\>\> \~/.bashrc. After reloading the configuration, the terraform
version command executed successfully, confirming that Terraform was
properly installed and accessible.

During the installation process, the main challenge encountered was
related to environment variable configuration, particularly the
inconsistency between Windows PATH settings and Git Bash. This issue was
resolved by explicitly exporting the Terraform path within the Git Bash
environment.

In conclusion, Terraform was successfully installed and configured.
Despite minor challenges with PATH recognition in Git Bash, the issues
were effectively diagnosed and resolved, resulting in a fully functional
setup ready for use.
