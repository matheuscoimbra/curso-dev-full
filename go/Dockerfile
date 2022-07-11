FROM golang:alpine3.16 as build
WORKDIR /app
COPY hello.go ./
RUN go build hello.go

FROM scratch
COPY --from=build /app .
ENTRYPOINT ["./hello"]