# fastapi-azure-app
A minimal FAST API app to experiment with Azure cloud deployment

## Running the app locally

```bash
# clone the repo
$ git clone https://github.com/bytefull/fastapi-azure-app.git
$ cd fastapi-azure-app

# create a virtual environment and activate it
$ pipenv shell

# install the required packages inside the virtual environment
$ pipenv install

# run the application
$ uvicorn app:app --reload --log-level debug
```

## The app is deployed on Azure [here](https://fastapiapp.azurewebsites.net/docs)
Azure app service will internally use this command to run the app

```bash
$ gunicorn app:app --workers 4 --worker-class uvicorn.workers.UvicornWorker --reload
```
