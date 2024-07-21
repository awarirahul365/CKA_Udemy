FROM python:3.6-alpine

RUN pip install flask

COPY . /opt/

EXPOSE 8080

WORKDIR /opt

ENTRYPOINT ["python", "app.py"] # If Docker file , Then Entrypoint is Command and CMD is argument . Enrtypoint starts at start of the container and CMD 

CMD ["--color", "red"]

kubectl replace --force -f /tmp/kubectl-edit-1744531591.yaml

kubectl run --help