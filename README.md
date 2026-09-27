# 🎨 AI Neural Style Transfer using AdaIN

An **AI-based Neural Style Transfer** project that combines the content of one image with the artistic style of another image using **Adaptive Instance Normalization (AdaIN)**.

The project provides a web-based interface where users can upload a **content image** and a **style image**, and generate a new image that preserves the content while applying the selected artistic style.

## ✨ Features

* 🖼️ Upload a content image
* 🎨 Upload a style image
* 🤖 Neural Style Transfer using AdaIN
* ⚡ Fast image stylization using a pretrained VGG encoder and decoder
* 🌐 Simple web interface
* 📥 Generate and view stylized output
* 🔄 Supports different combinations of content and style images

## 🧠 How It Works

The project uses **Adaptive Instance Normalization (AdaIN)** for neural style transfer.

The basic process is:

```text
Content Image ──┐
                ├──> VGG Encoder ──> AdaIN ──> Decoder ──> Stylized Image
Style Image ────┘
```

### Main Steps

1. The **content image** and **style image** are passed through a pretrained VGG encoder.
2. AdaIN aligns the feature statistics of the content image with those of the style image.
3. The transformed features are passed through a decoder.
4. The decoder reconstructs the final **stylized image**.

## 🛠️ Technologies Used

* Python
* PyTorch
* Flask
* NumPy
* OpenCV / PIL
* HTML & CSS
* VGG-19
* Adaptive Instance Normalization (AdaIN)

## 📁 Project Structure

```text
ai-nst-project/
│
├── NST_Code/
│   ├── app.py
│   ├── train.py
│   ├── utils/
│   │   ├── models.py
│   │   └── utils.py
│   │
│   ├── templates/
│   │   └── index.html
│   │
│   ├── content_data/
│   ├── style_data/
│   └── examples/
│
├── requirements.txt
├── Procfile
├── README.md
└── .gitignore
```

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/ai-nst-project.git
cd ai-nst-project
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## ▶️ Running the Project

Run the Flask application:

```bash
python NST_Code/app.py
```

Then open the local server in your browser.

```text
http://127.0.0.1:5000/
```

Upload a content image and a style image to generate the stylized result.

## 📸 Example

### Input

**Content Image + Style Image**

### Output

**Stylized Image**

The model preserves the main structure and content of the original image while transferring the visual characteristics of the style image.

## 📌 Model Weights

The pretrained model weights are not included in this repository because of their large file size.

Required model files include:

```text
vgg_normalised.pth
decoder_final.pth
```

Place the required weights in their corresponding directories before running the application.

## 🔬 About AdaIN

**Adaptive Instance Normalization (AdaIN)** is a technique used for real-time arbitrary style transfer.

Unlike methods that require training a separate model for every style, AdaIN allows different styles to be transferred using the same framework.

This makes it possible to combine many different content and style images without retraining the entire network.
  
---

⭐ If you found this project interesting, consider giving the repository a star!
