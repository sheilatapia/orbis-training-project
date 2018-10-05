docker build -t sheilatapia/orbis-training-docker:0.1.0 .

docker push sheilatapia/orbis-training-docker:0.1.0

docker tag sheilatapia/orbis-training-docker:0.1.0 sheilatapia/orbis-training-docker:0.2.0
docker push sheilatapia/orbis-training-docker:0.2.0

docker run -it -p 1080:80 sheilatapia/orbis-training-docker:1.0.0