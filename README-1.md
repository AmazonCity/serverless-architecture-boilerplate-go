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

# 

### @islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ go run mage.go build

go: downloading github.com/magefile/mage v1.11.0
go: downloading github.com/aws/aws-lambda-go v1.13.3
go: downloading github.com/google/uuid v1.1.1
go: downloading github.com/aws/aws-sdk-go v1.27.2
go: downloading github.com/jmespath/go-jmespath v0.0.0-20180206201540-c2b33e8439af

### @islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ go run mage.go deploy

Error: failed to run "serverless deploy --verbose --force: exec: "serverless": executable file not found in $PATH"
exit status 1

### @islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ npm install -g serverless

npm WARN deprecated querystring@0.2.1: The querystring API is considered Legacy. new code should use the URLSearchParams API instead.
npm WARN deprecated querystring@0.2.0: The querystring API is considered Legacy. new code should use the URLSearchParams API instead.
npm WARN deprecated querystring@0.2.0: The querystring API is considered Legacy. new code should use the URLSearchParams API instead.
npm WARN deprecated superagent@7.1.6: Please downgrade to v7.1.5 if you need IE/ActiveXObject support OR upgrade to v8.0.0 as we no longer support IE and published an incorrect patch version (see https://github.com/visionmedia/superagent/issues/1731)

added 407 packages in 29s

67 packages are looking for funding
  run `npm fund` for details
npm notice 
npm notice New minor version of npm available! 9.5.0 -> 9.6.3
npm notice Changelog: https://github.com/npm/cli/releases/tag/v9.6.3
npm notice Run npm install -g npm@9.6.3 to update!
npm notice 

@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ serverless --version

Framework Core: 3.29.0
Plugin: 6.2.3
SDK: 4.3.2

### @islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ pwd 

/workspaces/serverless-architecture-boilerplate-go

@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ nano ~/.bashrc

@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ source ~/.bashrc

@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ go run mage.go deploy

To ensure safe major version upgrades ensure "frameworkVersion" setting in service configuration (recommended setup: "frameworkVersion: ^3.29.0")


Deploying serverless-go to stage dev (us-east-1)

Excluding development dependencies for service package

✖ Stack serverless-go-dev failed to deploy (2s)
Environment: linux, node 19.7.0, framework 3.29.0, plugin 6.2.3, SDK 4.3.2
Docs:        docs.serverless.com
Support:     forum.serverless.com
Bugs:        github.com/serverless/serverless/issues


1 deprecation found: run 'serverless doctor' for more details
Error: running "serverless deploy --verbose --force" failed with exit code 1
exit status 1

@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ serverless doctor

1 deprecation triggered in the last command:

Starting with version 4.0.0, following property will be replaced:
  "provider.iamRoleStatements" -> "provider.iam.role.statements"
More info: https://serverless.com/framework/docs/deprecations/#PROVIDER_IAM_SETTINGS_V3

@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $  serverless --org=amazoncity

? No AWS credentials found, what credentials do you want to use? Local AWS Access Keys
? Do you have an AWS account? Yes

If your browser does not open automatically, please open this URL: https://console.aws.amazon.com/iam/home?region=us-east-1#/users$new?step=final&accessKey&userNames=serverless&permissionType=policies&policies=arn:aws:iam::aws:policy%2FAdministratorAccess


                    M? In your AWS account, create an AWS user with access keys. Then pres
? In your AWS account, create an AWS user with access keys. Then press [Enter] to 
continue. 

? AWS Access Key Id: AKI************GDG

? AWS Secret Access Key: BE4************************P2Y

✔ AWS credentials saved on your machine at "~/.aws/credentials". Go there to change them at any time.

? Do you want to deploy now? Yes

Deploying serverless-go to stage dev (us-east-1)

✔ Service deployed to stack serverless-go-dev (210s)

endpoints:

  POST - https://b2xktu6613.execute-api.us-east-1.amazonaws.com/dev/books
  
  GET - https://b2xktu6613.execute-api.us-east-1.amazonaws.com/dev/books
  
  GET - https://b2xktu6613.execute-api.us-east-1.amazonaws.com/dev/books/{hashkey}
  
  PUT - https://b2xktu6613.execute-api.us-east-1.amazonaws.com/dev/books/{hashkey}
  
  DELETE - https://b2xktu6613.execute-api.us-east-1.amazonaws.com/dev/books/{hashkey}
 ``` 
functions:

  create: serverless-go-dev-create (24 MB)
  read: serverless-go-dev-read (24 MB)
  read_detail: serverless-go-dev-read_detail (24 MB)
  update: serverless-go-dev-update (24 MB)
  delete: serverless-go-dev-delete (24 MB)
  worker: serverless-go-dev-worker (24 MB)
```
What next?
Run these commands in the project directory:
```
serverless deploy    Deploy changes
serverless info      View deployed endpoints and resources
serverless invoke    Invoke deployed functions
serverless --help    Discover more commands
```
1 deprecation found: run 'serverless doctor' for more details

@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ serverless doctor

1 deprecation triggered in the last command:

Starting with version 4.0.0, following property will be replaced:
  "provider.iamRoleStatements" -> "provider.iam.role.statements"
More info: https://serverless.com/framework/docs/deprecations/#PROVIDER_IAM_SETTINGS_V3

@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ 

@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ serverless info
```
service: serverless-go
stage: dev
region: us-east-1
stack: serverless-go-dev
endpoints:
  POST - https://b2xktu6613.execute-api.us-east-1.amazonaws.com/dev/books
  GET - https://b2xktu6613.execute-api.us-east-1.amazonaws.com/dev/books
  GET - https://b2xktu6613.execute-api.us-east-1.amazonaws.com/dev/books/{hashkey}
  PUT - https://b2xktu6613.execute-api.us-east-1.amazonaws.com/dev/books/{hashkey}
  DELETE - https://b2xktu6613.execute-api.us-east-1.amazonaws.com/dev/books/{hashkey}
functions:
  create: serverless-go-dev-create
  read: serverless-go-dev-read
  read_detail: serverless-go-dev-read_detail
  update: serverless-go-dev-update
  delete: serverless-go-dev-delete
  worker: serverless-go-dev-worker
```

1 deprecation found: run 'serverless doctor' for more details

@islamicity24 ➜ /workspaces/serverless-architecture-boilerplate-go (main) $ serverless --help

Serverless Framework v3.29.0

Usage
serverless <command> <options>
sls <command> <options>

Get started
Run serverless to interactively setup a project.
Use --help-interactive to display the interactive setup help.

Monitoring
Enable performance and error monitoring with the Serverless Dashboard.
Learn more: https://serverless.com/monitoring

Plugins
Extend the Serverless Framework with plugins.
Explore plugins: https://serverless.com/plugins
```
Options
--help / -h                     Show this message
--version / -v                  Show version info
--verbose                       Show verbose logs
--debug                         Namespace of debug logs to expose (use "*" to display all)

Main commands
deploy                          Deploy a Serverless service
deploy function                 Deploy a single function from the service
info                            Display information about the service
invoke                          Invoke a deployed function
invoke local                    Invoke function locally
logs                            Output the logs of a deployed function

Other commands
deploy list                     List deployed version of your Serverless Service
deploy list functions           List all the deployed functions and their versions
metrics                         Show metrics for a specific function
remove                          Remove Serverless service and all resources
rollback                        Rollback the Serverless service to a specific deployment
rollback function               Rollback the function to the previous version
test                            Run HTTP tests
package                         Packages a Serverless service
plugin install                  Install and add a plugin to your service
plugin uninstall                Uninstall and remove a plugin from your service
print                           Print your compiled and resolved config file
config                          Configure Serverless
config credentials              Configures a new provider profile for the Serverless Framework
create                          Create new Serverless service
dashboard                       Open the Serverless dashboard
doctor                          Print status on reported deprecations triggered in the last command run
generate-event                  Generate event
help                            Show this help
install                         Install a Serverless service from GitHub or a plugin from the Serverless registry
login                           Login or sign up for Serverless
logout                          Logout from Serverless
output get                      Get value of dashboard deployment profile parameter
output list                     List all dashboard deployment profile parameters
param get                       Get value of dashboard service output
param list                      List all dashboard deployment profile parameters
plugin list                     Lists all available plugins
plugin search                   Search for plugins
slstats                         Enable or disable stats
```
