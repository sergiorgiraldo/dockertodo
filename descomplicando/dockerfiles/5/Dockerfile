FROM golang AS building

WORKDIR /app
ADD . /app
RUN go build hello.go

FROM alpine
WORKDIR /tux
COPY --from=building /app/hello /tux

ENTRYPOINT ./hello

