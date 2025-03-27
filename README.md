
https://github.com/data-science-on-aws/



# Attend our Free, Online, Full-Day Workshop!
You must register on [**Eventbrite**](https://www.eventbrite.com/e/full-day-workshop-kubeflow-gpu-kerastensorflow-20-tf-extended-tfx-kubernetes-pytorch-xgboost-tickets-63362929227).  

_All instructions will come through Eventbrite.  Please make sure your Eventbrite email address is up to date._

# Upcoming O'Reilly Book:  _Data Science on AWS_
Register for early access directly on our [**website**](https://datascienceonaws.com).

Request one of our [**talks**](https://datascienceonaws.com) for your conference or meetup.

[![Data Science on AWS](img/data-science-on-aws-book.png)](https://datascienceonaws.com)

# Workshop Cost - FREE
This workshop is FREE, but would otherwise cost <25 USD.

![Workshop Cost](img/billing.png)

# Workshop Agenda
[![Workshop Agenda](img/outline.png)](https://www.eventbrite.com/e/full-day-workshop-kubeflow-gpu-kerastensorflow-20-tf-extended-tfx-kubernetes-pytorch-xgboost-tickets-63362929227)

# Workshop Instructions
_Note:  This workshop will create an ephemeral AWS acccount for each attendee.  This ephemeral account is not accessible after the workshop.  You can, of course, clone this GitHub repo and reproduce the entire workshop in your own AWS Account._

## 0. Logout of All AWS Consoles Across All Browser Tabs
If you do not logout of existing AWS Consoles, things will not work properly.

![AWS Account Logout](img/aws-logout.png)

_Please logout of all AWS Console sessions in all browser tabs._

## 1. Login to the Workshop Portal (aka Event Engine). 

![Event Box Event Engine Account](img/eb-aws-account-clean.png) 

![Event Box Launch](img/launch.png)

![Event Engine Terms and Conditions](img/event-engine-terms.png)

![Event Engine Dashboard](img/event-engine-dashboard.png)


## 2. Login to the **AWS Console**

![Event Engine AWS Console](img/event-engine-aws-console.png)

Take the defaults and click on **Open AWS Console**. This will open AWS Console in a new browser tab.

If you see this message, you need to logout from any previously used AWS accounts.

![AWS Account Logout](img/aws-logout.png)

_Please logout of all AWS Console sessions in all browser tabs._

Double-check that your account name is similar to `TeamRole/MasterKey` as follows:

![IAM Role](img/teamrole-masterkey.png)

If not, please logout of your AWS Console in all browser tabs and re-run the steps above!


## 3. Launch a SageMaker Notebook Instance

Open the [AWS Management Console](https://console.aws.amazon.com/console/home)

**Note:** This workshop has been tested on the US West (Oregon) (us-west-2) region. Make sure that you see **Oregon** on the top right hand corner of your AWS Management Console. If you see a different region, click the dropdown menu and select US West (Oregon).

In the AWS Console search bar, type `SageMaker` and select `Amazon SageMaker` to open the service console.

![SageMaker Console](img/setup_aws_console.png). 

Select `Create notebook instance`.

![SageMaker Console](img/aws-sagemaker-dashboard.png).

![SageMaker Console](img/create-notebook-instance.png)

In the Notebook instance name text box, enter `workshop`.

Choose `ml.c5.2xlarge`. We'll only be using this instance to launch jobs. The training job themselves will run either on a SageMaker managed cluster or an Amazon EKS cluster.

Volume size `250` - this is needed to explore datasets, build docker containers, and more.  During training data is copied directly from Amazon S3 to the training cluster when using SageMaker.  When using Amazon EKS, we'll setup a distributed file system that worker nodes will use to get access to training data.

![Fill notebook instance](img/notebook-setup01.png)

In the IAM role box, select the default `TeamRole`.

![Fill notebook instance](img/notebook-setup02.png)

Click `Create notebook instance`.

![Fill notebook instance](img/notebook-setup03-no-vpc.png)


## 4. Start the Jupyter Notebook

_Note:  Proceed when the status of the notebook instance changes from `Pending` to `InService` after a few minutes._

![Start Jupyter](img/start_jupyter.png)


## 5. Launch a New Terminal within the Jupyter Notebook

Click `File` > `New` > [...scroll down...] `Terminal` to launch a terminal in your Jupyter instance.

![](img/launch_jupyter_terminal.png)


## 6. Clone this GitHub Repo in the Terminal

Within the Jupyter terminal, run the following:

```
cd ~/SageMaker && git clone https://github.com/data-science-on-aws/workshop
```

![](img/clone-workshop-repo.png)

**REPEATING AGAIN - THIS IS IMPORTANT - MAKE SURE YOU RUN THIS IN THE JUPYTER TERMINAL**
```
cd ~/SageMaker && git clone https://github.com/data-science-on-aws/workshop
```


## 7. Navigate Back to Notebook View

![](img/back-to-jupyter-notebook.png)


## 8. Start the Workshop!
Navigate to `01_setup/` in your Jupyter notebook and start the workshop!

_You may need to refresh your browser if you don't see the new `workshop/` directory._

![Start Workshop](img/start_workshop.png)
