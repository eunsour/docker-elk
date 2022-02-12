ARG ELK_VERSION

FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

RUN elasticsearch-plugin install analysis-nori
RUN elasticsearch-plugin install analysis-phonetic
# RUN elasticsearch-plugin install https://github.com/eunsour/kodex/releases/download/7.14.1/eunsour_KodexTokenFilter-7.14.1.zip
