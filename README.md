# Streamlit_test
Testing if you can deploy streamlit app to azure or aws

## 1. Try to make it work locally github codespace

-Reference 1 - [https://gabrielecalvo.github.io/p/streamlit-on-azure/]


-Reference 2 - [https://medium.com/towards-data-science/beginner-guide-to-streamlit-deployment-on-azure-f6618eee1ba9]


-Docker Running Process Reference [https://docs.streamlit.io/knowledge-base/tutorials/deploy/docker]

-Reference 3 [https://towardsdatascience.com/deploying-a-streamlit-web-app-with-azure-app-service-1f09a2159743]


## 2. Commands to run docker

    1. If you first time run this, need to build docker image. build docker image by running this : docker build -t streamlit .
    2. See the image list by typing this : docker images
    3. You will see this 
        REPOSITORY   TAG       IMAGE ID       CREATED              SIZE
        streamlit    latest    70b0759a094d   About a minute ago   1.02GB
    4 Run the docker container by typing this:  docker run -p 8501:8501 streamlit

## we finally get it run on auzre app service

    Push the docker file to azure image registory through main.yml file from the workflow --- after trigering the action which will create a work flow and automaticall push it to the azure image registory. 

    you however need to mannually deploy the image to azure app service. make sure choose the right setting. Do not add command line since you have entry point from docker file.



