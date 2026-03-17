**Installation and Configuration of AWS CLI**

The installation of the AWS Command Line Interface (AWS CLI) was carried
out on a Windows 11 system as part of setting up a cloud development
environment.

To begin, the official installation guide provided by Amazon Web
Services was consulted via the AWS documentation page. The recommended
installation method for Windows using the MSI installer was followed.

The installation was initiated directly from the terminal using Git Bash
with the command:

msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi

This command downloaded and launched the AWS CLI version 2 installer
package. The installation process completed successfully without errors,
following the default setup configuration.

After installation, the AWS CLI was verified by running the command:

aws \--version

The output returned:

aws-cli/2.31.5 Python/3.13.7 Windows/11 exe/AMD64

This confirmed that the AWS CLI was correctly installed and accessible
from the terminal.

Following installation, AWS credentials were configured and verified
using the command:

aws sts get-caller-identity

The output was:

{

  \"UserId\": \"AIDAXXXXXXXX\",

  \"Account\": \"123456789012\",

  \"Arn\": \"arn:aws:iam::123456789012:user/MyUsername\"

}

This verified that the AWS CLI was properly connected to the AWS
account, with credentials correctly recognized and active.

During the installation and configuration process, no major challenges
were encountered. The installation was straightforward due to the use of
the MSI package, which automatically handled configuration and system
integration. Additionally, the AWS CLI was immediately recognized in the
terminal environment, and credentials were successfully applied,
confirming full operational readiness.

In conclusion, the AWS CLI was successfully installed, configured, and
verified. The process was smooth and efficient, providing a functional
command-line tool for interacting with AWS services, which is essential
for cloud and DevOps operations.
