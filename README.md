# fusionpbx-labs
Deploy Fusionpbx - Debian 10 (Buster) and PHP 7.3

# Build docker image:
docker build --rm -t {name_of_image} --file Dockerfile .

# Run Docker container:
docker run --rm --net=host --privileged --name {name_of_container} {name_of_image}

# Change DB user password
docker exec {name_of_container} sudo -u postgres psql -c "ALTER USER fusionpbx WITH PASSWORD 'newpassword';"
