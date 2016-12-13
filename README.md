This script courtesy of [coreysa](https://github.com/coreysa)

Details for running it can be found on [Scott Hanselman's Blog](http://www.hanselman.com/blog/GettingAdminByAddingANewUserToSudoersWhenYoureLockedOutOfAnAzureLinuxVM.aspx)

I take no credit for any of this :)

Instructions for use:
1. Edit CustomScriptConfig.json and append your desired username and password after the 'sh useradd.sh', so it looks like `"commandToExecute":"sh useradd.sh myuser mypass"`
2. From AzureCLI, run `azure vm extension set -c "/path/to/CustomScriptConfig.json" -g <resource group name> -m <vm name> -n CustomScriptForLinux -p Microsoft.OSTCExtensions -o 1.5`
