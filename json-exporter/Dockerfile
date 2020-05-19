FROM golang:1.14-alpine3.11 AS build

RUN apk --no-cache add git && \
    go get github.com/tolleiv/json-exporter 

CMD [ "/bin/sh" ]

#----------------------------------------------------
FROM alpine:3.11

COPY --from=build /go/bin/json-exporter /usr/local/bin/json-exporter

CMD [ "/usr/local/bin/json-exporter" ]


