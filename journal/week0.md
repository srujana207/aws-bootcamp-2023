# Week 0 — Billing and Architecture

## Prerequisite Technologies checklist

1. Github account done
2.  Gitpod account done
3.  Github Codespaces account done
4.  AWS account done
5.  Lucid Chart account done
6. Honeycomb.io account done
7. Rollbar account done



## Summary

In week 0 of the bootcamp, we were introduced to a Business scenario and a good idea as to how it works in real life companies. We were also made aware of the "Iron triangle" and how it works according to the requirement of the company. A "Good Architecture" must be thorough about its RRACs which is Requirements, Risks, Assumptions and Constraints. We were also introduced to C4 model and TOGAF model which is for visualizing the software architecture. We were given a brief on requirement gathering and how it is important to "Devlop a common dictionary", ask "dumb questions", "pretend to be the end user" and make sure to "document everything". Design types were also covered
* Conceptual Design : understanding and requirement gathering of the work. *Intial idea
* Logical Design : Functional blocks of conceptual design. *Blueprint
* Physical Design : Actual Design of logical design. *Implementation

## Homework challenges

### 1. Set MFA

* Created AWS free tier account 
* Go to IAM 
* Enable MFA
  1.  Go to Assign MFA if not assigned
  2.  Specify name
  3.  Choose MFA device. I have selected Google Authenticator as my authenticator device. Downloaded in my phone, Scanned the code and connected to the account.
  4.  Enter the 2 MFA codes.
  5.  Click Add MFA. 


### 2. Create IAM User


### 3. Set IAM Roles
* Go to Roles in the left hand side of  AWS IAM
* Click  "Create roles"
* In AWS Service Policies, Select EC2
* In Add Permissions, Select AdminstartorAccess or whichever policy/policies
* Provide Name, Description
* Add meaningful tag
* Click "Create role"

#### MFA

![MFA](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/image.png "MFA enabled")

#### IAM User

![IAM user](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/iam.png "IAM user created")

#### IAM Role

![IAM role](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/iam%20role.png "IAM role craeted")




### 3. Logical and Napkin diagrams


![Napkin design](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Picsart_23-02-28_01-07-47-891.jpg "Napkin Diagram")


#### Lucid chart image of the Logical Diagram


![Lucid chart Logic](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Blank%20diagram_%20Lucidchart.png "Lucid Chart diagram Logical")


#### The above Lucid chart is [linked] as follows


### Conceptual diagram

![Lucid chart conceptual](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/conceputal%20diagram.png "Lucid chart diagram conceptual")

#### The above is my recreated version of the conceptual diagram of Cruddur. The Lucid chart diagram is aslo linked [here].


### 4. Installed and configured AWS CLI

#### Installation

* Open search engine
* Type in "AWS CLI download"
* Click [this] link 
*  Scroll down to "AWS CLI install and update instructions"
*  Click on the "Windows" drop down
*  Follow the instructions
   1. Under the "1. Download and run the AWS CLI MSI installer for Windows (64-bit):", click the [given link]
   2. Click on "Next", accept the terms and conditions and click on "Next"  until "Finish".
   3. You have completed the installation
   4. Now to check the installation is successful, open command prompt, type in "aws --version". If it provides the version written as under "2. To confirm the installation, open the Start menu, search for cmd to open a command prompt window, and at the command prompt use the aws --version command.", then you have successfully installed the AWS CLI.

#### Configuration

* To configure(ie. connect AWS CLI to the AWS account), we require "Access Key" and "secret Key". 
   1. If already created, proceed to next steps. 
   2. If creating from Root account, go to "My security credentials", scroll down to "Access keys" and click on "Create access key".
   3. If creating from IAM user account, go to "IAM", click on "Users from the left panel, select the user and scroll down to "Access keys" and click on "create access key".
* After the above steps are completed, we are taken to a space where we ahve to select the purpose of the keys (what are they being used for?). As we are connecting to AWS CLI, we choose the first option "Command Line Interface (CLI)
You plan to use this access key to enable the AWS CLI to access your AWS account."
* Checkbox the "I understand the above recommendation and want to proceed to create an access key." and click "Next".
* Add some meaningful tag, click "Create access key".
* The access keys are created. Download details by clicking on "Download .csv file".
* Go back to command prompt, type "aws configure"
   1. Copy and paste the "AWS Access key Id" in the prompt, click enter.
   2. Copy and paste "AWS Secret key" and click enter.
   3. Enter "Default region name", clcik enter.
   4. Enter "Deafult output format", click enter (here, none so directly click enter).
* You have connected AWS CLI to the Account.
* Type in "aws iam list-users" in the propmt to check. If output displayed is correct, you have successfully configured AWS CLI

### 5. Billing and Budget

#### Enabling Billing alarms

* Go to Billing.
* Select Billing Preferences from the left hand side.
* Check box the following

  1. recieve PDF invoice by email
  2. Recieve free tier usage by alerts and fill in the email address where you'd like to recieve the alerts
  3. Recieve Billing alerts
* Click Save Preferences
* Now, go to Manage Billing Alerts highlighted.
* This will redirect you to CloudWatch Management Console.
* Select Alarms from the left hand side.
* Select In Alarms under it.
* Go to Create alarms.
* Choose the Select metric option under the 1. Specify and conidtions.
*  Select option under Browse, here, Billing as we are creating billing alarms.
* Choose the option from the provided options, here, Total Estimated Charge.
* Choose USD as currency.
* Click on Select metric. We have successfully completed selecting the metrics for the graph of the billing estimates.
* Provide the metric name as required. Select the options for Conditions, here, Static as Threshold type, Greater as Whenever week0EstimatedCharges is... and any value, here, 1 as than.
* Click on Next.
*  In the 2. Configure actions, choose In alarm in Alarm state trigger.
*  Select Create new topic from Send a notification to the following SNS topic. Enter the name of the SNS topic name and email endpoint. Click on Create topic. Successfully configured what to do when the amout goes above the threshold value mentioned.
*  Enter the name and enter a brief description (in Markdown language) of the purpose of the alarm in the 3. Add name and description. Click Next.
*  As the last step 4. Preview and create suggests, verify the entered deatils and click on Create alarm.
*  Go to All alarms. The alarm will be successfully created. 


#### Creating Budget

* Go to Billing.
* Select Budgets from the left hand side.
* Click Create budget.
* Choose options from Choose budget setup. Here, in Budget setup, choose Use a template(simplified).
* From Templates - new, choose an option. Here, select Monthly cost budget. Give a name, amount and email address and click on Create budget. You have succesfully created a buddget, which notifies to the mentioned email address when the amount exceeds the given value.




[linked]: https://lucid.app/lucidchart/b3129d64-4cb4-4e46-ad79-33ccdbecaf54/edit?viewport_loc=-766%2C-420%2C2560%2C1116%2C0_0&invitationId=inv_76e4f070-6ec2-46ea-802e-3764c3975101

[here]: https://lucid.app/lucidchart/941b6e3a-7255-4f07-ae22-b560077ad9d8/edit?viewport_loc=3%2C54%2C2567%2C1116%2C0_0&invitationId=inv_15ce3798-cb5a-460c-987e-4e98dbde89db

[this]: https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

[given link]: https://awscli.amazonaws.com/AWSCLIV2.msi






> 
