# Microsoft-Azure-Machine-Learning-Engineer-Udacity-Project-2

The project includes an AutoML model setup on the Bank Marketing Dataset as part of this project, deployed the best model that resulted from the run as a RESTful API Webservice, used endpoints to communicate with the deployed model in ML studio, and finally automated pipelines to enhance machine learning operations.

## Architectural Diagram

<img width="778" alt="image" src="https://user-images.githubusercontent.com/110788191/233855841-efefda4f-9848-4fd3-ac3d-94d359ba1e5e.png">


## Key Steps

### Authentication

Platforms and systems can run automatically and without interruption thanks to a sort of authentication termed a "Service Principal". Access to resources in Microsoft Azure is authenticated and authorized via a service principal, a type of Azure Active Directory (AAD) application. It depicts a machine-generated thing, such a program or a script.
Service Principals are typically used in instances when human involvement would be impracticable or would slow down the process, such as automated scripts, DevOps pipelines, or other systems requiring programmatic access to Azure services. You can use a Service Principal to grant the necessary permissions and access to certain resources without using a human user account, helping to maintain the system's security and integrity.

Within Azure resources, Service Principals can be given particular responsibilities and permissions, giving them more precise control over what tasks they can complete. This means that Service Principals are only given the rights necessary to carry out their assigned tasks, lowering the risk of unwanted access. These permissions are set based on the principle of least privilege.

In conclusion, employing Service Principals for authentication and automation can assist preserve security and reduce the need for human intervention in some situations, all while ensuring an uninterrupted flow of operations.

### AutoML

Automated Machine Learning, often known as Azure AutoML, is a service offered by Microsoft Azure that streamlines the creation, training, and deployment of machine learning models without the need for advanced data science or machine learning knowledge. It makes AI capabilities more widely available to a wider group of users, including business analysts and domain experts, by streamlining the machine learning workflow and democratizing access to it.

Machine learning models are automatically selected, preprocessed, and optimized by Azure AutoML using a graphical user interface (GUI) and automated algorithms, making it simpler for users to create high-performing models without writing a lot of code. Among Azure AutoML's essential elements are:

### Data preparation: 
Azure AutoML makes it simple for users to import, purge, and preprocess data from a variety of sources, including CSV files, SQL databases, and Azure Blob storage. For customers to better understand their data and spot any concerns with data quality, it has built-in data visualization and data profiling tools.

### Model selection and training: 
Azure AutoML automatically chooses the best machine learning algorithm from a variety of choices based on the input data and task type, such as classification, regression, or time-series forecasting. The performance of the models is then assessed using methods like cross-validation after they have been automatically trained using various hyperparameter combinations.

### Evaluation and interpretation of the model: 
Azure AutoML offers metrics and visualizations to assist customers in assessing the effectiveness of trained models and choosing the top model for their particular use case. Additionally, it offers elements for model interpretability, such as feature importance, that aid users in understanding the significance of various aspects in the model's predictions.

### Monitoring and deployment: 
After a model is chosen, Azure AutoML enables customers to quickly and easily deploy it as a web service, allowing them to include the trained model into their applications. Additionally, it gives users the ability to monitor and manage their models in production by tracking the usage and performance of deployed models.

Azure AutoML enables customers to build fully automated machine learning pipelines that handle everything from model development through data preparation automatically. This makes machine learning efficient and consistent by allowing users to build reusable, scaleable procedures for various use cases.

Overall, Azure AutoML makes it easier for users of all skill levels to design, train, and deploy machine learning models, driving the adoption of machine learning across a range of industries and domains.

1. The best trained model is delivered into production during a model's deployment so that it can be used by others. The VotingEnsemble model, which has the highest accuracy of 0.94607, is the best model discovered during the AutoML run. By enabling authentication and using Azure Container Instance (ACI), which quickly deploys compute instances to deploy models, we configured the deployment settings while deploying the model. Additionally, using it is really straightforward.

2. A vital step in the process before enabling Application Insights is enabling logging. A technology that aids in finding abnormalities and visualizing performance is called application insights. It can be changed with the SDK and activated before or after the deployment. In this project, we extend the Python SDK with particular commands to provide application insights after deployment. Python script that has been changed to display logs.

3. The excellent tool Swagger makes it easy to create, describe, and use RESTful API webservices that are installed in Azure Machine Learning Studio. It goes on to explain the many categories of HTTP requests that an API can handle, in this case Post, Get, and Update. The endpoints area of Azure offers a swagger.json that is used to build a website. This localhost webpage describes a deployed model's HTTP endpoint. The homepage displays the contents of the API for the best model along with the various HTTP queries that are supported after the swagger.sh and serve.py scripts have been executed.

4. Finally, an HTTP API is used to consume the deployed service. In order to submit data, we start an input request, in this example using the HTTP Post request method. Another request approach to get data from a web server is an HTTP GET request. As a result, Azure now has a two-way flow of authorized information. The URI and key are modified to match the primary key for our service in order to consume deployed services, and a RESTful URI is generated after deployment. The output is produced when the endpoint.py script is executed following change.


## 2. Automated ML  Experiment:
## 2.1 Registered Dataset:

Our a dataset is registered in Azure Machine Learning, it becomes a reusable entity that can be referenced in experiments, pipelines, and deployments, facilitating collaborative data-driven development.

<img width="1042" alt="Dataset_register" src="https://user-images.githubusercontent.com/110788191/233704283-3a5e9ce9-5764-44d9-bfd0-030b83c7f00d.png">

## 2.2 Dataset Guradrail:

Dataset gets checked for test cases ensuring data quality.

<img width="1438" alt="Screenshot 2023-04-23 at 02 42 24" src="https://user-images.githubusercontent.com/110788191/233813399-8b99c2d4-b5f0-47d9-9b85-94d220dbd048.png">

## 2.3 Completed Run:

The screenshot shows an completed run of our automL job.

<img width="1433" alt="image" src="https://user-images.githubusercontent.com/110788191/234662582-3bc4952e-b6a3-4514-883f-12d2e4e88bf3.png">

<img width="1439" alt="Screenshot 2023-04-21 at 20 03 54" src="https://user-images.githubusercontent.com/110788191/233704768-e547afd0-6d99-4e0f-9e31-5d76d08d416e.png">

## 2.4 Best Model:

After an sucessfull automl job, the best model was Voting Ensembler with an accuracy of 0.94.

<img width="1191" alt="best_model" src="https://user-images.githubusercontent.com/110788191/233704981-1ab167aa-81d8-4302-8f4b-424ff966aad4.png">

## Best Model- Feature Importance

The model also has explaibilty regrading the feature engineering occured during the training.

<img width="1439" alt="Screenshot 2023-04-23 at 02 43 10" src="https://user-images.githubusercontent.com/110788191/233813404-76dd4bb9-6687-4c5e-a32e-5d9c2902fdce.png">

## Best Model- Metrics
Following evaluations metrics gets logged into the metric section of the job.

<img width="1435" alt="Screenshot 2023-04-23 at 02 43 40" src="https://user-images.githubusercontent.com/110788191/233813431-c10f2cf9-629b-432d-83c1-1925a144aacc.png">

## 3 Model Deployment

Deploying the Best Model on ACI will allow to interact with the HTTP API service and interact with the model by sending data over POST requests. 
Also enabling authentication.

<img width="1433" alt="model deployment" src="https://user-images.githubusercontent.com/110788191/233812998-df66fce9-89a6-4dc4-bc9a-fd8e8b721c7b.png">

## 4 Enable Logging

The Best Model is deployed, enable Application Insights and retrieve logs. The screenshot depicts the dashboard for monitoring different metrics.

Screenshot depicting app insights enabled.

<img width="1433" alt="model deployment" src="https://user-images.githubusercontent.com/110788191/233812998-df66fce9-89a6-4dc4-bc9a-fd8e8b721c7b.png">

<img width="1439" alt="app insights dashboard" src="https://user-images.githubusercontent.com/110788191/233813036-f193df6d-822f-4b9d-a23f-0fcd65ec1f2e.png">

## 4.1 App Insights logging

Now that the Best Model is deployed, enabling Application Insights and retrieve logs. Editing the provided **logs.py** and running it on notebook results in enabling logs of the deployed model. 

<img width="1436" alt="image" src="https://user-images.githubusercontent.com/110788191/234669368-4dab6afe-0e08-4f3c-a9ed-cd5587512a07.png">

Also available in model deployments log section.

<img width="1433" alt="image" src="https://user-images.githubusercontent.com/110788191/234669973-51f37993-bf10-478d-a130-7c159531d966.png">

## 5 Swagger 

Azure provides a Swagger JSON file for deployed models. 
Swagger runs on localhost showing the HTTP API methods and responses for the model. Sucessfull calls using **serve.py** HTTP API methods and responses for the model. Running **swager.sh** for geeting docker image.

Sucessfull calls using serve.py HTTP API methods and responses for the model. Running swager.sh for geeting docker image.


<img width="1439" alt="image" src="https://user-images.githubusercontent.com/110788191/234680689-3baf679d-7f83-438e-b6d1-aaeaada7c911.png">

<img width="1434" alt="image" src="https://user-images.githubusercontent.com/110788191/234681019-cac3d69e-1076-4bde-9c2b-327990576222.png">


<img width="1439" alt="image" src="https://user-images.githubusercontent.com/110788191/234677504-5fb915dc-cf47-4681-a1ea-80b02effd902.png">

<img width="1437" alt="image" src="https://user-images.githubusercontent.com/110788191/234675719-4044f56d-6df2-4d80-9d74-869010b049c0.png">


## 6 Consume Endpoints

Running endpoint.py for getting json output from the model. The screenshots depicts the successfull calls.

<img width="913" alt="api-test" src="https://user-images.githubusercontent.com/110788191/233813151-6a77aafa-e5f7-4989-83b8-91a5cd03fba4.png">

<img width="812" alt="logs2" src="https://user-images.githubusercontent.com/110788191/233813155-6a5ab7bc-37eb-48f0-bc67-c6788e2335c4.png">

<img width="903" alt="logs" src="https://user-images.githubusercontent.com/110788191/233813158-fbff5914-a944-4b50-9ede-d050cc8c5070.png">

Also testing in json foramt in UI.

<img width="1426" alt="image" src="https://user-images.githubusercontent.com/110788191/234678350-67af8017-8010-4bfc-9a6a-46b97b257f79.png">



## 7 Create, Publish and Consume a Pipeline:

The screenshot depicts the published pipeline with auto_ml step.

<img width="1437" alt="image" src="https://user-images.githubusercontent.com/110788191/234671161-69744e21-f9a6-4f8f-99fe-e826115d2a5d.png">

<img width="1439" alt="pipeline" src="https://user-images.githubusercontent.com/110788191/233708107-435e2ceb-81b4-400f-9d00-8fe1984f51a7.png">

## Pipeline Endpoint

The published pipeline of with auto_ml step is now available as an API in pipeline_endpoint section.

<img width="1440" alt="pipeline_endpoint" src="https://user-images.githubusercontent.com/110788191/233708295-4e4a8946-47cd-419a-95b7-76f9a8ba0ea5.png">

## Pipeline Endpoint Status

The API endpoint status is Active in pipeline_endpoint section.

<img width="1436" alt="Screenshot 2023-04-23 at 02 49 43" src="https://user-images.githubusercontent.com/110788191/233813524-80ad27bb-334a-4e0b-9fb6-07e280961ec6.png">

## Jupyter Notebook Screenshots

You can also have a look at successfull notebook in the code repository. 

Screenshot

<img width="1213" alt="image" src="https://user-images.githubusercontent.com/110788191/234674579-19b8cf38-933c-47dc-bc0d-5a7dd857a37c.png">

<img width="1216" alt="image" src="https://user-images.githubusercontent.com/110788191/234675913-330e2e4a-6d17-4be6-87d5-c40fd2f986e3.png">

Screenshot depicting child runs summary.

<img width="1433" alt="image" src="https://user-images.githubusercontent.com/110788191/234676096-a1973aab-68ed-4cb1-ba2f-3ae06b15c09e.png">

Retruving Best Model.

<img width="1216" alt="image" src="https://user-images.githubusercontent.com/110788191/234676899-0e8a89c5-985a-4e83-836e-f92e480b20fe.png">


Publishing pipeline snippet from notebook.

<img width="1435" alt="image" src="https://user-images.githubusercontent.com/110788191/234676381-793e03e2-3d0c-4e6e-b92a-551813358c7c.png">

<img width="1437" alt="image" src="https://user-images.githubusercontent.com/110788191/234676669-0da12e63-dc51-40af-85e4-2900c3704a5b.png">

<img width="1440" alt="pipeline_endpoint" src="https://user-images.githubusercontent.com/110788191/233708295-4e4a8946-47cd-419a-95b7-76f9a8ba0ea5.png">

<img width="1436" alt="Screenshot 2023-04-23 at 02 49 43" src="https://user-images.githubusercontent.com/110788191/233813524-80ad27bb-334a-4e0b-9fb6-07e280961ec6.png">


## Future Improvements

A useful technique for evaluating a deployed model's performance and confirming that it adheres to expectations is benchmarking. A popular command-line tool for measuring response time in seconds and assessing model effectiveness is Apache Benchmark (ab).

The ideal model can be found by experimentation, but it's vital to take cost considerations into account, especially when running models on a Virtual Machine (VM). Finding the ideal setup requires balancing various elements, including resource costs, parallel processing, and experiment duration.

A container orchestration technology called Kubernetes might be useful for managing resources and scaling up or down in response to demand. When more data is added to the existing dataset, it can also aid in the efficient deployment and utilization of resources, thereby lowering costs.

Monitoring and logging: Setting up reliable systems for tracking the performance of the deployed model can provide us insights into how it behaves and point out areas where it can be improved.

Automated testing: By include automated testing in the deployment pipeline, performance regressions and other problems can be discovered early on, allowing for prompt correction.

Techniques for optimization: Investigating optimization methods like model quantization, model trimming, or hardware acceleration might enhance the performance of the deployed model while consuming less resources.

Cost management while preserving performance can be achieved by routinely reviewing and improving resource utilization, such as by shrinking virtual machines or configuring Kubernetes clusters more effectively.

Security considerations: To protect sensitive information and preserve compliance, it is essential to make sure that the benchmarking and experimentation processes follow security best practices, such as data protection, access controls, and secure communication.

In conclusion, benchmarking, trying out various models, utilizing tools like Kubernetes, and taking into account additional elements like monitoring, automated testing, optimization techniques, cost optimization, and security considerations can all help to ensure that a deployed model performs to expectations.

