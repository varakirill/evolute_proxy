FROM ghcr.io/home-assistant/aarch64-base:latest

ENV LANG=C.UTF-8

RUN apk add --no-cache \
        python3 \
        py3-pip \
    && pip3 install --no-cache-dir --break-system-packages --upgrade pip \
    && pip3 install --no-cache-dir --break-system-packages flask requests

COPY run.sh /run.sh
COPY evolute_api.py /evolute_api.py

RUN chmod a+x /run.sh

CMD [ "/run.sh" ]