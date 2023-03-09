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

In week 0 of the bootcamp, we were introduced to a Business scenario and a good idea as to how it works in real life companies. We were also made aware of the "Iron triangle" and how it works according to the requirement of the company. A "Good Architecture" must be thorough about its RRACs which is Requirements, Risks, Assumptions and Constraints. We were also introduced to C4 model and TOGAF model which is for visualizing the software architecture. We were given a brief on requirement gathering and how it is important to "Devlop a common dictionary", ask "dumb questions", "pretend to be the ned user" and make sure to "document everything". Design types were also covered
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

### 2. Set IAM Roles
* Go to Roles in the left hand side of  AWS IAM
* Click  "Create roles"
* In AWS Service Policies, Select EC2
* In Add Permissions, Select AdminstartorAccess or whichever policy/policies
* Provide Name, Description
* Add meaningful tag
* Click "Create role"

![MFA](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/image.png "MFA enabled")

![IAM user](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/iam.png "IAM user created")

![IAM role]( "IAM role craeted")


### 3. Logical and Napkin diagrams


![Napkin design](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Picsart_23-02-28_01-07-47-891.jpg "Napkin Diagram")


#### Lucid chart image of the Logical Diagram


![Lucid chart Logic](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/Blank%20diagram_%20Lucidchart.png "Lucid Chart diagram Logical")


#### The above Lucid chart is [linked] as follows


### Conceptual diagram

![Lucid chart conceptual](https://github.com/srujana207/aws-bootcamp-cruddur-2023/blob/main/journal/assets/conceputal%20diagram.png "Lucid chart diagram conceptual")

#### The above is my recreated version of the conceptual diagram of Cruddur. The Lucid chart diagram is aslo linked [here].

### CI/CD pipeline conceptual diagram


![Lucid chart CI/CD]( "Lucid chart diagram CI/CD")

#### The above is my recreated version of the conceptual diagram of the CI/CD pipeline. This is the [link] of the Lucid chart diagram.


[linked]: https://lucid.app/lucidchart/b3129d64-4cb4-4e46-ad79-33ccdbecaf54/edit?viewport_loc=-766%2C-420%2C2560%2C1116%2C0_0&invitationId=inv_76e4f070-6ec2-46ea-802e-3764c3975101

[here]: https://lucid.app/lucidchart/941b6e3a-7255-4f07-ae22-b560077ad9d8/edit?viewport_loc=3%2C54%2C2567%2C1116%2C0_0&invitationId=inv_15ce3798-cb5a-460c-987e-4e98dbde89db

[link]: https://lucid.app/lucidchart/2750f61a-8249-43b4-a627-626c7974d2a6/edit?viewport_loc=-10%2C-10%2C1707%2C821%2C0_0&invitationId=inv_d76973e3-0b30-4660-a75e-f91f80b742dc






> 
