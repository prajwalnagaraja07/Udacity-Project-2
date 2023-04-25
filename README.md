# Microsoft-Azure-Machine-Learning-Engineer-Udacity-Project-2

The project includes an AutoML model setup on the Bank Marketing Dataset as part of this project, deployed the best model that resulted from the run as a RESTful API Webservice, used endpoints to communicate with the deployed model in ML studio, and finally automated pipelines to enhance machine learning operations.

## Architectural Diagram
<img width="903" alt="image" src="https://user-images.githubusercontent.com/110788191/234421411-9074b7c1-a5b8-4f54-bd00-957f71eb2f18.png">
 

## Key Steps
### Registered Dataset:

<img width="1042" alt="Dataset_register" src="https://user-images.githubusercontent.com/110788191/233704283-3a5e9ce9-5764-44d9-bfd0-030b83c7f00d.png">

### Dataset Guradrail:
<img width="1438" alt="Screenshot 2023-04-23 at 02 42 24" src="https://user-images.githubusercontent.com/110788191/233813399-8b99c2d4-b5f0-47d9-9b85-94d220dbd048.png">

### Completed Run:
<img width="1439" alt="Screenshot 2023-04-21 at 20 03 54" src="https://user-images.githubusercontent.com/110788191/233704768-e547afd0-6d99-4e0f-9e31-5d76d08d416e.png">

### Pipeline Published:

<img width="1439" alt="pipeline" src="https://user-images.githubusercontent.com/110788191/233708107-435e2ceb-81b4-400f-9d00-8fe1984f51a7.png">

### Pipeline Endpoint

<img width="1440" alt="pipeline_endpoint" src="https://user-images.githubusercontent.com/110788191/233708295-4e4a8946-47cd-419a-95b7-76f9a8ba0ea5.png">

### Pipeline Endpoint Status

<img width="1436" alt="Screenshot 2023-04-23 at 02 49 43" src="https://user-images.githubusercontent.com/110788191/233813524-80ad27bb-334a-4e0b-9fb6-07e280961ec6.png">

### Best Model:
<img width="1191" alt="best_model" src="https://user-images.githubusercontent.com/110788191/233704981-1ab167aa-81d8-4302-8f4b-424ff966aad4.png">


### Best Model- Feature Importance
<img width="1439" alt="Screenshot 2023-04-23 at 02 43 10" src="https://user-images.githubusercontent.com/110788191/233813404-76dd4bb9-6687-4c5e-a32e-5d9c2902fdce.png">

### Best Model- Metrics
<img width="1435" alt="Screenshot 2023-04-23 at 02 43 40" src="https://user-images.githubusercontent.com/110788191/233813431-c10f2cf9-629b-432d-83c1-1925a144aacc.png">


### Model Deployment
<img width="1433" alt="model deployment" src="https://user-images.githubusercontent.com/110788191/233812998-df66fce9-89a6-4dc4-bc9a-fd8e8b721c7b.png">

### App Insights
<img width="1439" alt="app insights dashboard" src="https://user-images.githubusercontent.com/110788191/233813036-f193df6d-822f-4b9d-a23f-0fcd65ec1f2e.png">


### Swagger CLI
<img width="1436" alt="swagger" src="https://user-images.githubusercontent.com/110788191/233813092-5559ff17-e4f6-4d9b-abb5-00e48c1c4930.png">

### Swagger API Call

<img width="1440" alt="serve" src="https://user-images.githubusercontent.com/110788191/233813127-cd267dc8-16e1-4f46-93a0-2fc2ad2aa4f1.png">

### API Test

<img width="913" alt="api-test" src="https://user-images.githubusercontent.com/110788191/233813151-6a77aafa-e5f7-4989-83b8-91a5cd03fba4.png">

<img width="812" alt="logs2" src="https://user-images.githubusercontent.com/110788191/233813155-6a5ab7bc-37eb-48f0-bc67-c6788e2335c4.png">

<img width="903" alt="logs" src="https://user-images.githubusercontent.com/110788191/233813158-fbff5914-a944-4b50-9ede-d050cc8c5070.png">


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


