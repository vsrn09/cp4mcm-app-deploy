# Deploying Mattermost App on Openshift Cluster using CP4MCM deployment model

Mattermost is an open source Slack-alternative used by thousands of companies around the world in 14 languages. Learn more at [https://about.mattermost.com](https://about.mattermost.com/).

1. Login to your OpenShift environment by copying your login credentials from the Openshift UI.

   ```shell
   oc login --token=<your_token> --server=<https://c107-e.us-south.containers.cloud.ibm.com:32613>
   ```

2. Clone the github repo

   ```shell
   git clone https://github.ibm.com/vsrn09/cp4mcm-app-deploy.gitRun the following command to install create a namespace and create a channel

   ```shell
   oc apply -f resources/00-application.yaml
   ```
   ```

3. Run the following command to create an application

   ```shell
   oc apply -f resources/04-app.yaml
   ```

4. Run the following command to create a subscription rule

   ```shell
   oc apply -f resources/03-subscription.yaml
   ```

5. Run the following command to install create a namespace and create a channel

   ```shell
   oc apply -f resources/00-application.yaml
   ``` 


6. Run the following command to create a placement rule

   ``` shell
   oc apply -f resources/02-placement-rule.yaml
   ```

7. Run the following command to deploy all the requied artifacts for mattermost app

  ```shell
  oc apply -f resources/01-mattermost-deployable.yaml
  ```



8. Run the following command on the managed cluster/s

   ```shell
   oc apply -f resources/image-policy.yaml
   ```

 