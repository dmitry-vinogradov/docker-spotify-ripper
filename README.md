Dockerfile for spotify-ripper (https://github.com/jrnewell/spotify-ripper)

Build from docker file

git clone https://github.com/darrenwatt/docker-spotify-ripper.git
cd docker-spotify-ripper
cp -pr example.config.ini config.ini
#edit config to suit
vi config.ini
docker build -t spotify-ripper .

Start with

docker run -d -h your_host_name -v /your_download_location:/data --name spotify-ripper spotify-ripper

Send commands with

docker exec spotify-ripper spotify-ripper spotify:track:52xaypL0Kjzk0ngwv3oBPR
