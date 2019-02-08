FROM openjdk:8-jre

ADD . /owlsim
WORKDIR /owlsim

RUN gzip -d all.owl.gz
RUN gzip -d owlsim.cache.gz
RUN chmod +x owltools

CMD ./owltools all.owl --use-fsim  --sim-load-lcs-cache owlsim.cache --sim-load-ic-cache ic-cache.owl --start-sim-server -p 9031

EXPOSE 9031
