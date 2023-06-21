# sunlit_notebooks
Notebooks related to sunlit.ai

## Installation for kaggle_tutorial.ipynb

### Create new conda environment
conda create -n learn_nlp2 python=3.9
conda activate learn_nlp2

### Install conda dependencies
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
conda install -c huggingface -c conda-forge datasets jupyterlab kaggle pandas
pip uninstall tokenizers
pip install transformers[torch]
python -c "from transformers import pipeline; print(pipeline('sentiment-analysis')('we love you'))"
Should print out [{'label': 'POSITIVE', 'score': 0.9998704791069031}]

### Download model
mkdir models
cd models
git lfs install
git clone git@hf.co:microsoft/deberta-v3-small

### install bert model dependencies
pip install sentencepiece wandb ipywidgets
pip uninstall protobuf
pip install protobuf==3.19.0

### Now can run the notebook