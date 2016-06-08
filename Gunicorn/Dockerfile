# Run gunicorn in a container
#
# docker run -i -t \
#        -v $HOME/Data:/home/data  \  <- mounts data directory to container
#        toddstavish/gunicorn
#
FROM ubuntu:14.04
MAINTAINER Todd Stavish <toddstavish@gmail.com>

# Install binary dependencies
RUN apt-get -qqy update && \
    apt-get install -qqy \
        python \
        python-dev \
        python-pip \
        git-all \
        --no-install-recommends

# Install gunicorn
RUN pip install gunicorn

# Pull project
COPY myapp.py /

# Clean-up
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Open port 8000
EXPOSE 8000

# Run gunicorn
ENTRYPOINT ["/usr/local/bin/gunicorn"]
CMD ["-b", ":8000", "myapp:app"]
#CMD ["/bin/bash"]
