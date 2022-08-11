FROM public.ecr.aws/amazonlinux/amazonlinux:latest

# Install dependencies
RUN yum update -y && \
    yum install -y python3 && \
    yum install -y python3-pip && \
    pip3 install numpy && \
    pip3 install awsiotsdk 

# run selected files
RUN mkdir /pyfiles
COPY ./dummy_sensor.py /pyfiles/dummy_sensor.py
COPY ./example_publisher.py /pyfiles/example_publisher.py

EXPOSE 80

CMD ["python3","-u", "/pyfiles/example_publisher.py"]
