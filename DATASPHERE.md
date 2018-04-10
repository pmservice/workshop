# DataSphere ML&DL Workshops
Watson Machine Learning Workshops

## Prerequisities:

### Signing up for a free trial

0. If you already have a IBM Cloud account, you can sign in to IBM Cloud at https://www.ibm.com/cloud/. Otherwise follow step 1 to create IBM Cloud account.

1. Go to https://www.ibm.com/cloud and sign up for a free trial and register for IBM Cloud.

### Services provisioning
2. Go to `Catalog` (https://console.bluemix.net/catalog/) and create instances of the following services (**Lite** plan should be chosen):
  - Cloud Object Storage
  - Watson Machine learning
  - Apache Spark
  - Watson Studio

![catalog_view](images/catalog.jpg)


## Creating a new project in IBM Watson Studio
3. Open Watson Studio created instance and click `Get Started` button

4. Once signed in, click on the tile that says `New project`. Scroll to the bottom to find the tile for `Jupyter Notebooks`. Select it and press OK.

![welcome_page](images/ws_welcome.jpg)

5. Follow the instructions and fill in the details for new project  on the left panel.

6. Great, you have covered the first milestone.

![project_view](images/project.jpg)


## Scenario 1: Product purchase prediction with Spark MLlib

**Description**: Within this scenario you will develop spark mllib model to predict product purchases. Next you will deploy this model as web service and bind sample web  application to it. The application will send scoring records to deployed model and display predicted purchases.

### Jupyter Notebook
1. In project `Settings tab` - `Associated services` section link your spark sevice instance with the project.

2. Create `(+) New notebook` from [file](https://dataplatform.ibm.com/analytics/notebooks/v2/d5e46fc8-3ea5-4982-a161-032905a2c42a/view?access_token=5cd484379907747b0e0e6a99d5546bcac8e39fb22268c7e0ff618db8c4e3c4bd).

  **Tip**: download sample notebook from url using download button and use it as a notebook file. Select `Spark` as a runtime environment for the notebook.
3. Execute notebook cells. Make sure that your Watson Machine Learning service credentials are put in cell [29].

  **Tip**: you can find your credentials on the service `credentials` tab (IBM Cloud Dashboard).

4. Great, you have covered the first part of scenario.

### Node.js application

Since our model is deployed as a web service it is a time to provide sample web application that will send scoring records to `scoring_endpoint` and in return present purchases predictions.

1. Deploy product line prediction [application](https://github.com/pmservice/product-line-prediction) to your Cloud account. Follow up [Application deployment](https://github.com/pmservice/product-line-prediction#application-deployment) steps (Deploy to IBM Cloud button).

2. Open IBM Cloud Dashboard and select deployed application. In `Connections` tab connect your app to Watson Machine Learning service.

3. You are all set - run the app by clicking `Visit App URL`.


## Scenario 2: Style transfer with Keras
**Description**: In this scenario you will learn how to run deep learning experiment to transfer style from famous painting (e.g. Picasso) to your photo.

### Jupyter Notebook
1. Create `(+) New notebook` from [file](https://dataplatform.ibm.com/analytics/notebooks/v2/b21d09ab-728f-4e70-a0cc-dcee9a395a9e/view?access_token=5f23e9fae56ca858df6795ec2d5b3bde9f5ff1224258f0f4703ea9327fd210b9).


### Python web application
