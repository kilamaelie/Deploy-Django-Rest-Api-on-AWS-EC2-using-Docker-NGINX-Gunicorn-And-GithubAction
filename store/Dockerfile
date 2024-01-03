
FROM python:alpine3.19

# Prevents Python from writing pyc files.
ENV PYTHONDONTWRITEBYTECODE=1

# Keeps Python from buffering stdout and stderr to avoid situations where
# the application crashes without emitting any logs due to buffering.
ENV PYTHONUNBUFFERED=1

WORKDIR /store

RUN pip install --upgrade pip
COPY ./requirements.txt /store/requirements.txt
RUN pip install -r /store/requirements.txt


# Copy the source code into the container.
COPY . .


