# REST API using Golang  


###### Note: Make sure your go environment is correctly setup for development.

Run the below commands in order on commandline
```python
# Install the glide package manager
curl https://glide.sh/get | sh

# Clone the boilerplate project
https://github.com/satishgolang/GoProject

cd rest-api

# (Optional) Update the dependencies
glide update

# Installs all dependencies in project vendor folder.
glide install

# builds the application and creates a binary go-rest-api
go build

# Run the API server
GO_ENV_PORT=8000 ./go-rest-api-boilerplate
```

OR
Run the following docker commands
```python
cd rest-api

# Build the docker image
docker build -t rest-api.
# Run the API in a container. Replace <free_port_on_host> with 8000
docker run -p <free_port_on_host>:8000 rest-api
```

### Check the API output
```
curl http://localhost:8000/v1/users/1
```
Expected Output:
```
{"ID":0,"CreatedAt":"0001-01-01T00:00:00Z","UpdatedAt":"0001-01-01T00:00:00Z","DeletedAt":null,"age":35,"first_name":"Amrendra","last_name":"singh"}
```
===================================================================================
```
curl http://localhost:8000/v1/users
```
Expected Output:
```
[{"ID":0,"CreatedAt":"0001-01-01T00:00:00Z","UpdatedAt":"0001-01-01T00:00:00Z","DeletedAt":null,"age":35,"first_name":"satish","last_name":"loyapally"},{"ID":0,"CreatedAt":"0001-01-01T00:00:00Z","UpdatedAt":"0001-01-01T00:00:00Z","DeletedAt":null,"age":35,"first_name":"Amrendra","last_name":"singh"}]
```
