<!--- [instructions: quick start](#Quick-Start)

[instructions: detailed](#Detailed-Setup-Instructions)-->

### Simplified batch experimentation with Watson Studio
Executing batch experiments in Watson Studio was designed to be flexibile and to fit into a range of pre-existing workflows. However this flexibility can be daunting for new users.  Now executing experiments is as simple as:

```
experiment = Experiment("My experiment", "Test hyperparameter range",
                        "tensorflow", "1.5", "python","3.5",
                        studio_utils, project_utils)
                        
experiment.add_training_run("cnn tests", hyperparams, "python3 experiment.py", "experiment.zip", "v100x2")
experiment.execute()
```

The utility classes below hide the underlying complexity while the source code for everything's available so you can dig deeper as you advance.  

<p align="center">
  <img width=500 src="media/utils_explained.png?">
</p>

To help you get started, [sample experiments are available for standard use cases]().  These samples are designed for quick execution from the command prompt but can be easily inserted into a notebook if desired.

### Quick Start
The next section provides detailed setup instructions, but if you're already familiar with Watson Studio and IBM Cloud service, it's a simple 4-step process. (1) clone this repository then (2) [install the Watson Machine Learning (WML) python client](https://wml-api-pyclient-dev.mybluemix.net/).  (3)  copy credentials to [wml_credentials.json](settings/wml_credentials.json) and [cos_credentials.json](settings/cos_credentials.json) then (4) [execute the sample batch experiments]().

<p align="center">
  <img src="media/getting_started.png?">
</p>

### Detailed Setup Instructions
If you are new to Watson Studio or simply want more details on confguring the credentials files, then follow these steps:

1. [Install IBM Cloud's developer utilities](https://console.bluemix.net/docs/cli/index.html#overview)
2. Create WML services + credentials
   - [Using Watson Studio UI](wiki/Create-WML-Service)
   - [Using CLI]()
3. Create COS service + credentials
   - [Using Watson Studio UI](wiki/Create-COS-Service)
   - [Using CLI]()
4. [Create a project in Watson Studio and save the project id]()
5. [Execute example batch experiments]()

