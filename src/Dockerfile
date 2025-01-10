
ARG TARGETPLATFORM = "linux/amd64"

FROM --platform=$TARGETPLATFORM python:3.11-slim

ENV PUBLIC_URL_ENV=http://localhost:8000

WORKDIR /app

RUN pip install importlib-metadata==4.13 && \
    pip install enigmatui==1.0.2 && \
    pip install textual-serve==1.0.2 && \
    pip install textual-web==0.7.0 && \
    pip install textual-dev==1.7.0

EXPOSE 8000

COPY entrypoint.sh /app/entrypoint.sh

RUN chmod +x /app/entrypoint.sh

ENTRYPOINT ["./entrypoint.sh"]