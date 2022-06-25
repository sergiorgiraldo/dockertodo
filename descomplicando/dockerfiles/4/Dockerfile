FROM golang

WORKDIR /app
ADD . /app
RUN go build hello.go
ENTRYPOINT ./hello
