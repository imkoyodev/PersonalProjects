FROM python:3.12.6-alpine3.20 AS base

RUN apk update && apk --update add build-base linux-headers && apk cache clean
RUN apk add geos-dev gdal-dev proj-dev proj-util netcdf-dev hdf5-dev && apk cache clean
RUN pip --no-cache-dir install --upgrade pip
RUN pip --no-cache-dir install poetry==1.8.3 && pip cache purge
RUN poetry config virtualenvs.create false