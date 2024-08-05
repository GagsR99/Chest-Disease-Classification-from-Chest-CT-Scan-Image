# Chest-Disease-Classification-from-Chest-CT-Scan-Image

 - [Data link](https://drive.google.com/file/d/1z0mreUtRmR-P-magILsDR3T7M6IkGXtY/view?usp=sharing)

## Workflows

1. Update config.yaml
2. Update params.yaml
3. Update the entity
4. Update the configuration manager in src config
5. Update the components
6. Update the pipeline 
7. Update the main.py
8. Update the dvc.yaml 



## Live matarials docs

[link](https://docs.google.com/document/d/1UFiHnyKRqgx8Lodsvdzu58LbVjdWHNf-uab2WmhE0A4/edit?usp=sharing)


## Git commands

```bash
git add .

git commit -m "Updated"

git push origin main
```

## How to run?

```bash
conda create -n chest python=3.8 -y
```

```bash
conda activate chest
```

```bash
pip install -r requirements.txt
```

```bash
python app.py
```

### Mlflow dagshub connection uri

```bash
MLFLOW_TRACKING_URI=https://dagshub.com/GagsR99/Chest-Disease-Classification-from-Chest-CT-Scan-Image.mlflow \
MLFLOW_TRACKING_USERNAME=GagsR99 \
MLFLOW_TRACKING_PASSWORD=1ce0980a74e5c079f4b00a13426865357af3a8dc \
python script.py
```

```bash
import dagshub
dagshub.init(repo_owner='GagsR99', repo_name='Chest-Disease-Classification-from-Chest-CT-Scan-Image', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)
```


### RUN from bash terminal

```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/GagsR99/Chest-Disease-Classification-from-Chest-CT-Scan-Image.mlflow

export MLFLOW_TRACKING_USERNAME=GagsR99 

export MLFLOW_TRACKING_PASSWORD=1ce0980a74e5c079f4b00a13426865357af3a8dc

```



### DVC cmd

1. dvc init
2. dvc repro
3. dvc dag