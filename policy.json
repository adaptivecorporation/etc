from minio import Minio
from minio.error import ResponseError
import constants
import json

minioClient = Minio(
        '10.10.10.138:8080',
        access_key=constants.MINIO_ACCESS_KEY,
        secret_key=constants.MINIO_SECRET_KEY,
        secure=False,
    )

config = {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::345tyu-18da-4d9c-9a08-df456777/*"
            }
    ]
}

minioClient.set_bucket_policy("345tyu-18da-4d9c-9a08-df456777", json.dumps(config))



