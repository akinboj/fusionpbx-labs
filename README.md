# fusionpbx-labs
Deploy Fusionpbx in K8s

# Build docker image:
docker build --rm -t {name_of_image} --file Dockerfile .

# Run Docker container:
docker run --rm --net=host --privileged --name {name_of_container} {name_of_image}

# Change DB user password
docker exec {name_of_container} sudo -u postgres psql -c "ALTER USER fusionpbx WITH PASSWORD 'newpassword';"
