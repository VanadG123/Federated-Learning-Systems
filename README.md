# Federated-Learning-Systems

Developed a comprehensive federated learning system using Flower and PyTorch across three interconnected modules. Implemented a federated server application (FL_server_app.py) with custom metric aggregation and FedAvg strategy, created a client application (FL_client_app.py) for model training and evaluation, and designed a task module (FL_task.py) including a CNN model, data loading, and training routines. This system facilitates distributed training and evaluation of machine learning models, optimizing performance in a federated learning environment.

I have organized the model across three modules.

	1.	FL_server_app.py: This module sets up the federated learning server. It defines a custom metric aggregation function for weighted accuracy and configures the federated averaging strategy (FedAvg). The server initializes model parameters and coordinates the federated learning process by managing communication between clients and aggregating model updates. The ServerApp component orchestrates these tasks, ensuring efficient and accurate model training across distributed nodes.
	2.	FL_client_app.py: This file implements the client-side logic for federated learning. It defines a FlowerClient class that performs local model training and evaluation. The client trains a Convolutional Neural Network (CNN) on its local data using provided hyperparameters, then sends model updates back to the server. It supports training with the fit method and evaluating with the evaluate method, providing essential feedback for global model improvement.
	3.	FL_task.py: This module contains core functionalities for model architecture and data handling. It defines a simple CNN model and includes functions for loading and partitioning data, training, and testing. Utilizing the FederatedDataset library, it manages data preprocessing and transformation, ensuring effective model training and evaluation in a federated setup.

Together, these modules enable the development and deployment of a federated learning system, facilitating collaborative model training while preserving data privacy.
