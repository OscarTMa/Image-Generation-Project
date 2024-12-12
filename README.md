# Image Generation Project

## Table of Contents

1. [Description](#description)
2. [Dataset](#dataset)
3. [Models](#models)
4. [Features](#features)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Project Structure](#project-structure)
8. [Contributing](#contributing)
9. [License](#license)
10. [Authors](#authors)

## Description

This project demonstrates various image generation techniques using the Fashion MNIST dataset. The implemented models include:

- **GAN** (Generative Adversarial Networks)
- **DCGAN** (Deep Convolutional GAN)
- **CycleGAN**

Additionally, advanced techniques such as **Transfer Learning** and **Fine Tuning** are applied. The project includes an interactive API for generating images and provides deployment solutions using Docker and Kubernetes.

## Dataset

The **Fashion MNIST dataset** consists of 70,000 grayscale images of size 28x28 pixels, categorized into 10 different classes of clothing items. It is widely used as a benchmark dataset for computer vision tasks. More information about the dataset can be found [here](https://github.com/zalandoresearch/fashion-mnist).

## Models

The following models are implemented in this project:

- **GAN**: A basic architecture for generating images from noise using adversarial training.
- **DCGAN**: A convolutional variant of GAN, providing improved results for image data.
- **CycleGAN**: Used for unpaired image-to-image translation tasks.

## Features

- **Image Generation**: Generate realistic clothing item images from random noise.
- **Transfer Learning and Fine Tuning**: Leverage pre-trained models to enhance image generation quality.
- **Interactive API**: Create and serve generated images via a REST API built with Flask or FastAPI.
- **Deployment**: Containerize the application with Docker and orchestrate it using Kubernetes.

## Installation

### Prerequisites

Ensure you have the following installed:

- **Python 3.8+**
- **Docker**
- **Kubernetes** (Minikube or similar for local testing)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/oscartma/Image-Generation-Project.git
   cd Image-Generation-Project
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. (Optional) Set up a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

## Usage

### Running Notebooks

1. Navigate to the `notebooks/` directory.
2. Open and run the desired notebook using Jupyter or Google Colab.

### Running the API

1. Navigate to the `src/api/` directory.
2. Run the API server:
   ```bash
   python app.py
   ```
3. Access the API at `http://localhost:5000`.

### Deployment with Docker

1. Build the Docker image:
   ```bash
   docker build -t image-generation-api .
   ```
2. Run the container:
   ```bash
   docker run -p 5000:5000 image-generation-api
   ```

### Deployment with Kubernetes

1. Apply the deployment and service configurations:
   ```bash
   kubectl apply -f kubernetes/deployment.yaml
   kubectl apply -f kubernetes/service.yaml
   ```
2. Access the service using the provided Kubernetes endpoint.

## Project Structure

```
Image-Generation-Project/
|
├── README.md
├── notebooks/
│   ├── fashion_mnist_exploration.ipynb  # Dataset exploration and preprocessing.
│   ├── gan_training.ipynb               # GAN training notebook.
│   ├── dcgan_training.ipynb             # DCGAN training notebook.
│   ├── cyclegan_training.ipynb          # CycleGAN training notebook.
│
├── src/
│   ├── data/
│   │   ├── dataset_loader.py            # Dataset loading and preprocessing scripts.
│   │
│   ├── models/
│   │   ├── gan.py                       # GAN model implementation.
│   │   ├── dcgan.py                     # DCGAN model implementation.
│   │   ├── cyclegan.py                  # CycleGAN model implementation.
│   │
│   ├── api/
│   │   ├── app.py                       # REST API implementation.
│   │
│   ├── utils/
│       ├── metrics.py                   # Model evaluation metrics.
│       ├── visualization.py             # Visualization utilities.
│
├── Dockerfile                           # Docker configuration.
├── kubernetes/
│   ├── deployment.yaml                  # Kubernetes deployment configuration.
│   ├── service.yaml                     # Kubernetes service configuration.
│
├── requirements.txt                     # Python dependencies.
├── LICENSE
└── .gitignore
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any proposed changes or features.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Authors

- **[Oscar Tibaduiza](mailto:oscartibaduiza@hotmail.com)**


