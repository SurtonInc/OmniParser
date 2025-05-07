# Steps

1. **Clone the Repository**:
   Open your terminal and run the following command to clone the repository:

   ```bash
   git clone https://github.com/microsoft/Omniparser.git
   ```

2. **Install Dependencies**:
   Navigate to the cloned directory and install the required dependencies using pip:

   ```bash
   cd Omniparser
   pipenv install --python 3.12
   pipenv install huggingface[cli]
   ```

3. **Activate the Virtual Environment**:
   Activate the virtual environment created by pipenv:

   ```bash
   pipenv shell
   ```

4. **Download weights**
   Download the pre-trained weights for the model. You can do this by running the following command:

   ```bash
   huggingface-cli download microsoft/OmniParser-v2.0 --local-dir weights
   mv weights/icon_caption weights/icon_caption_florence
   ```

5. **Run the gradio demo** (optional):
   If you want to run the Gradio demo, you can do so by executing the following command:

   ```bash
   python gradio_demo.py
   ```

6. **Run the Omniparserserver**:
   To run the Omniparser server, execute the following command:

   ```bash
   cd omnitool/omniparserserver
   python -m omniparserserver
   ```
