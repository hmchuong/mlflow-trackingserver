# Demo MLFlow Tracking Server

## Clone the git repository
```bash
git clone https://github.com/hmchuong/mlflow-trackingserver
```

## Create virtual environment
Create python3 environment
```bash
virtualenv -p python3 env
```
Activate environment
```bash
source ./env/bin/activate
```

## Install dependencies
```bash
pip install mlflow==1.0
pip install google.cloud.storage
```

## Set up Google credential for tracking server
```bash
export GOOGLE_APPLICATION_CREDENTIALS=/Users/admin/projects/vietai-demo/mlflow-trackingserver/authen.json
```

## Start MLFlow tracking server
```bash
mlflow server \
    --backend-store-uri /tmp/tracking \
    --default-artifact-root gs://vietai-test/mlflow \
    --host 0.0.0.0
```
