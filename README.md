# AI Reference Architectures
This repository contains the recommended ways to train and deploy machine learning models on Azure. It ranges from running massively parallel [hyperparameter tuning using Hyperdrive](https://github.com/Microsoft/MLHyperparameterTuning) to deploying deep learning models on [Kubernetes](https://github.com/Microsoft/AKSDeploymentTutorialAML). Each [tutorial](#tutorials) takes you step by step through the process to train or deploy your model. If you are confused about what service to use and when look at the [FAQ](#faq) below.  

For further documentation on the reference architectures please look [here](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/).

# Getting Started
This repository is arranged as submodules and therefore you can either pull all the tutorials or simply the ones you want. 

<p align="center">
  <img width="800" src="./images/demo.svg">
</p>

To pull all the tutorials simply run:

```bash
git clone --recurse-submodules https://github.com/Microsoft/AIReferenceArchitectures.git
```

if you have git older than 2.13 run:

```bash
git clone --recursive https://github.com/Microsoft/AIReferenceArchitectures.git
```

# Tutorials <a name="tutorials"></a>
| Tutorial                                     | Environment | Description                                                                       | Status                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------|-------------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Deploy Deep Learning Model on Kubernetes](https://github.com/Microsoft/AKSDeploymentTutorialAML)    				   | Python GPU  | Deploy image classification model on Kubernetes for _real-time_ scoring             | [![Build Status](https://dev.azure.com/customai/AKSDeploymentTutorialAML/_apis/build/status/Microsoft.AKSDeploymentTutorialAML?branchName=master)](https://dev.azure.com/customai/AKSDeploymentTutorialAML/_build/latest?definitionId=11&branchName=master)                                                         |
| [Deploy Classic ML Model on Kubernetes](https://github.com/Microsoft/MLAKSDeployAML)       						   | Python CPU  | Train LightGBM model on local using Azure Machine Learning, deploy on Kubernetes for _real-time_ scoring                         | ![](https://dev.azure.com/customai/MLAKSDeployAMLPipeline/_apis/build/status/Microsoft.MLAKSDeployAML?branchName=master)                                                                                                                                                                                            |
| [Hyperparameter Tuning of Classical ML Models](https://github.com/Microsoft/MLHyperparameterTuning) 				   | Python CPU  | Train LightGBM model locally and run Hyperparameter tuning using Hyperdrive                            | ![](https://dev.azure.com/customai/MLHyperparameterTuningPipeline/_apis/build/status/Microsoft.MLHyperparameterTuning?branchName=master)                                                                                                                                                                            |
| [Deploy Deep Learning Model on Pipelines](https://github.com/Azure/Batch-Scoring-Deep-Learning-Models-With-AML)      | Python GPU  | Deploy style transfer model for _batch_ scoring using Azure ML Pipelines            | [![Build Status](https://dev.azure.com/customai/BatchScoringDeepLearningModelsWithAMLPipeline/_apis/build/status/Azure.Batch-Scoring-Deep-Learning-Models-With-AML?branchName=master)](https://dev.azure.com/customai/BatchScoringDeepLearningModelsWithAMLPipeline/_build/latest?definitionId=9&branchName=master) |
| [Deploy Classic ML Model on Pipelines](https://github.com/Microsoft/AMLBatchScoringPipeline)         				   | Python CPU  | Deploy one-class SVM for _batch_ scoring anomaly detection using Azure ML Pipelines | ![](https://dev.azure.com/customai/AMLBatchScoringPipeline/_apis/build/status/Microsoft.AMLBatchScoringPipeline?branchName=master)                                                                                                                                                                                  |
| [Deploy R ML Model on Kubernetes](https://github.com/Azure/RealtimeRDeployment)         							   | R CPU       | Deploy ML model for _real-time_ scoring on Kubernetes |  |
| [Deploy R ML Model on Batch](https://github.com/Azure/RBatchScoring)         										   | R CPU       | Deploy forecasting model for _batch_ scoring using Azure Batch and doAzureParallel |  | 
| [Deploy Spark ML Model on Databricks](https://github.com/Azure/BatchSparkScoringPredictiveMaintenance)         	   | Spark CPU   | Deploy one-class SVM for _batch_ scoring anomaly detection using Azure ML Pipelines |                                                                                                                                                                                 |
| [Train Distributed Deep Leaning Model](https://github.com/Azure/DistributedDeepLearning/)         				   | Python GPU  | Distributed training of ResNet50 model using Batch AI |                                                                                                                                                                                  |

# Requirements
The tutorials have been mainly tested on Linux VMs in Azure. Each tutorial may have slightly different requirements such as GPU for some of the deep learning ones. For more details please consult the readme in each tutorial.

## Reporting Issues
Please report issues with each tutorial in the tutorial's own github page.


# FAQ <a name="faq"></a>
* __What service should I use for deploying models in Python?__  
 If you are looking to deploy a model in Python for realtime or batch scoring look [here](docs/python_scoring.md).
* __What service should I use to train a model in Python?__  
For advice on what service to use to train a Deep Learning or classical ML model in Python look [here](docs/python_training.md).

# Recommend a Scenario
If there is a particular scenario you are interested in seeing a tutorial for please fill in a [scenario suggestion](https://github.com/Microsoft/AIReferenceArchitectures/issues/new?assignees=&labels=&template=scenario_request.md&title=%5BSCENARIO%5D)

## Ongoing Work
We are constantly developing interesting AI reference architectures using Microsoft AI Platform. Some of the ongoing projects include IoT Edge scenarios, model scoring on mobile devices, add more... To follow the progress and any new reference architectures, please go to the AI section of this [link](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/).

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
