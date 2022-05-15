# 9143-HPML-Project

- Project title: Voice Separation and Optimization in Recurrent Neural Networks
- Team members: Leo Hu, Junda Ai

---

# Spleeter

An optimizer modification of [Spleeter by deezer](https://github.com/deezer/spleeter/)

## Installation
Environment
```
# Install media/file dependencies using conda
conda install -c conda-forge ffmpeg libsndfile
# Clone spleeter repository
git clone https://github.com/Deezer/spleeter && cd spleeter
# Install poetry
pip install poetry
# Install spleeter dependencies
poetry install
# Run unit test suite
poetry run pytest tests/
```

To enable GPU
```
# Uninstall CPU tensorflow
pip uninstall tensorflow
# Install GPU tensorflow
pip install tensorflow-gpu==2.5.0
```

Modification
```
# Replace spleeter/model/__init__.py with __init__.py in spleeter_mod 
# Replace spleeter/__main__.py with __main__.py in spleeter_mod
# Place spleeter_entry.py in base directory

Modification Base/
├─ spleeter (forked)/
│  ├─ model/
│  │  ├─ __init__.py (modified)
│  ├─ __main__.py (modified)
├─ spleeter_entry.py
```

Preparation
```
# prepare the dataset: MUSDB18-HQ is used
# prepare the csv: based on dataset used
# modify the config: modify the links in the config file
```

## Training
- To test different optimizers, modify the `optimizer` item in the config file
- Logging frequency can be specified in `__main__.py`

when everything is ready:
```
python spleeter_entry.py train -p path/to/spleeter_config.json -d path/to/datasets --verbose
```

## 


---


# Svoice
[SVoice experiment](https://colab.research.google.com/drive/1B1cNeMLSL0KVs-Am1dKA5_F4E6k474_d#scrollTo=9DPpT3KiFTn2) was carried out on Google Colab.
