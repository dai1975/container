FROM golang:1.14.2-alpine3.11 as build

RUN apk --no-cache add git && \
    go get github.com/free/jiralert/cmd/jiralert

#-----------------------------------
FROM alpine:3.11

COPY --from=build /go/bin/jiralert /usr/local/bin/jiralert

CMD [ "/usr/local/bin/jiralert" ]
