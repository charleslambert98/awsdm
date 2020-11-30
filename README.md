# awsdm - AWS Distrbution Manager v. 1.2.0
A CLI program to make seamless changes to AWS lambda functions and S3 buckets, with a git connection. This script was created to make for the easy deployment of lambda functions and their dependencies to both AWS Lambda as well as a GitHub repository. The same applies to the S3 bucket file-deployment as well.

## Features

### awspush (--awspush)
This will handle the deployment of lambda code to AWS Lambda as well as GitHub for immediate deployment. Upon excution of this command, the user will be prompted with instructions to direct the program to the correct bot as well as the git commit and push information.

### s3push (--s3push)
This will handle the deployment of files to an AWS S3 bucket/path as well as GitHub for immediate usage. Upon execution of this command, the user will be prompted with instructions to direct the program to the correct bucket/path as well as the commit and push information. It is important to note that if there have been no changes made to the files being uploaded, then there will be no change to the S3 bucket.

### exit
Exits the program.

## Dependencies

- AWS CLI Version 2: https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html 
  - This is needed to make calls to AWS (make sure the account is configured)
- Git
  - This should be installed by default on most Unix systems

## Installation (Linux, MacOS ONLY)
**Note:** Please make sure that you have the above dependencies installed/configured!

1. Download the 'awsdm' file
2. Place the file in your `usr/local/bin` folder
3. Open your Terminal
4. Navigate to your `usr/local/bin` directory
5. Run the command `chmod a+rx awsdm` to make the file executable

## Usage

### Initialization
1. Stucture the File Path 
  - There should be two sub-folders
    - **lambda:** where AWS Lambda files are stored
    - **s3:** where S3 bucket files are stored
2. That's it!

### Common Usage
There are two ways that this program can be used:
1. Entering `awsdm [option]`
  - This will run once, then exit (preferred if performing one operation)
2. Entering the `awsdm` and choosing the option
  - This will run persistently, until exited (preferred if performing multiple operations)

**Note 1:** You must be in the root folder of the AWS program you wish to operate on. When running the program, all directory changes will be performed automatically.

**Note 2:** This information is also available through the use of the `awsdm --help` command

## Current Version Notes
- Will upload all files to the S3 bucket as **readable to the public**
