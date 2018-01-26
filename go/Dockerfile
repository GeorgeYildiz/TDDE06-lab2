FROM ubuntu:latest

#get sudo
RUN apt-get update && apt-get install -y sudo && rm -rf var/lib/apt/lists/*
RUN apt-get update

#get curl
RUN apt-get -y install curl

#get go 
RUN sudo curl -O https://storage.googleapis.com/golang/go1.9.1.linux-amd64.tar.gz
RUN sudo tar -xvf go1.9.1.linux-amd64.tar.gz
RUN sudo mv go /usr/local

#get git
RUN apt-get -y install git

#RUN export PATH=$PATH:/usr/local/go/bin
ENV PATH="/usr/local/go/bin:${PATH}"

#get go dependency
RUN go get github.com/lib/pq

COPY ./todo.go /usr/local/go_app/todo.go

RUN go build /usr/local/go_app/todo.go

EXPOSE 8080
CMD go run /usr/local/go_app/todo.go