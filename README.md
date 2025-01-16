# Description:

This repo contains an end-to-end recommender system model. The code base will contains two main parts:

* notebook: contains the modeling part(feature engineering and building recommender system model).
* service: contains microservice code to serve the model and deploy it to AWS.

Here are some useful commands to run the code locally:

# activate Virtual env:

```
virtualenv venv
python3 -m venv venv
source venv/bin/activate
pip3 install -r requirements.txt 
```

# install and open notebook from the virtual environment:

```
python -m pip install ipykernel
ipython kernel install --user --name=RecommederSystem
jupyter lab &
```

# Build docker image

cd service

docker build -t content-base-recommender .

# run docker container

docker run -d --publish 7777:5000 content-base-recommender

# make sure that the docker run locally (from docker):

http://localhost:7777/recommend/-1479311724257856983




The service is now ready to be pushed into ASW or AZURE
