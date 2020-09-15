FROM dtobtn/python-ml-base:latest

COPY read_score.py /app/
COPY docker/entrypoint.sh /app/
RUN chmod a+x /app/read_score.py
COPY docker/entrypoint.sh /app/
RUN chmod a+x /app/entrypoint.sh
COPY templates/ /app/templates/
WORKDIR /app

ENV FLASK_APP=read_score.py

ENTRYPOINT [ "/app/entrypoint.sh" ]


