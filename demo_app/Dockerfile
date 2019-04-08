# build stage
FROM golang:alpine AS build-env
ADD src /src
RUN cd /src && go build -o demo-app main.go

# final stage
FROM alpine
WORKDIR /app
COPY --from=build-env /src/demo-app /app/
EXPOSE 8080
ENTRYPOINT ./demo-app