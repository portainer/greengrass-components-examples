FROM public.ecr.aws/amazonlinux/amazonlinux:latest

# Install dependencies
RUN yum update -y && \
    yum install -y python3 && \
    yum install -y python3-pip && \
    pip3 install numpy && \
    pip3 install awsiotsdk 

# run selected files
RUN mkdir /pyfiles
COPY ./example_subscriber.py /pyfiles/example_subscriber.py

EXPOSE 80

CMD ["python3","-u", "/pyfiles/example_subscriber.py"]
