FROM dtobtn/python-ml-base:latest
RUN pip3 install beautifulsoup4
RUN pip3 install readability
RUN pip3 install lxml
RUN pip3 install readability-lxml
RUN pip3 install py-readability-metrics
COPY read_score.py /app/
COPY docker/entrypoint.sh /app/
RUN chmod a+x /app/read_score.py
COPY docker/entrypoint.sh /app/
RUN chmod a+x /app/entrypoint.sh
COPY templates/ /app/templates/
WORKDIR /app

ENV FLASK_APP=read_score.py

ENTRYPOINT [ "/app/entrypoint.sh" ]


