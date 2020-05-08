FROM alpine:3.11

RUN apk --no-cache add libintl && \
    apk --no-cache add --virtual .gettext gettext && \
    cp /usr/bin/envsubst /usr/local/bin/envsubst && \
    apk del .gettext

CMD [ "/bin/sh" ]
