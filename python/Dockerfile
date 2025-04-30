FROM docker.io/python:3-alpine
WORKDIR /usr/src/hostinfo
COPY ./host_info_server.py .
RUN chown 1000:1000 host_info_server.py && chmod 500 host_info_server.py && pip uninstall pip -y
LABEL org.opencontainers.image.ref.name=hostinfo
LABEL org.opencontainers.image.version=1.0.0-python
LABEL org.opencontainers.image.authors=rx-m
LABEL org.opencontainers.image.url=https://rx-m.com
USER 1000:1000
ENV PYTHONUNBUFFERED=1
ENTRYPOINT ["./host_info_server.py"]
CMD ["9898"]
