@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ go run mage.go deploy
Error: failed to run "serverless deploy --verbose --force: exec: "serverless": executable file not found in $PATH"
exit status 1


This error message indicates that the "serverless" executable file cannot be found in the system's PATH environment variable, which is necessary to execute the "serverless deploy" command.

To resolve this issue, you need to make sure that the Serverless Framework is installed on your system and added to the PATH environment variable. Here are the steps you can follow:

Install Serverless Framework by running the following command in your terminal:

```
npm install -g serverless
```
This command will install the Serverless Framework globally on your system.

Once the installation is complete, verify that the Serverless Framework is installed correctly by running the following command:

```
serverless --version
```
This command should return the version number of the Serverless Framework that you just installed.

If the Serverless Framework is installed correctly, you need to add it to the PATH environment variable. You can do this by adding the following line to your shell configuration file (e.g., ~/.bashrc, ~/.zshrc, etc.):

```
export PATH=$PATH:$(npm root -g)/serverless/bin
```
This line adds the Serverless Framework bin directory to your system's PATH environment variable.

After adding the line to your shell configuration file, save and close the file, and then run the following command in your terminal to refresh the PATH environment variable:

```
source ~/.bashrc
```
This command reloads the shell configuration file and updates the PATH environment variable.

Once you have completed these steps, you should be able to run the "serverless deploy" command without encountering the "executable file not found in $PATH" error.
