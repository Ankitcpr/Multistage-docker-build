###########################################
# Author: Ankit Kumar

# BASE IMAGE

# Date: 24/03/2024

# Version: v85.62

###########################################


# Base Image
FROM ubuntu AS build

# execute cmd
RUN apt-get update && apt-get install -y golang-go

# processing environment
ENV GO111MODULE=off

# copy from source directory to the current working directory
COPY . .

# executr
RUN CGO_ENABLED=0 go build -o /app .

# execute while creation of file
ENTRYPOINT ["/app"]


