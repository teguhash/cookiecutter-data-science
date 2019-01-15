Commands
========

The Makefile contains the central entry points for common tasks related to this project.

Syncing data to S3
^^^^^^^^^^^^^^^^^^

* `make sync_data_to_gcs` will use `gsutil -d -r rsync` to recursively sync files in `data/` up to `gs://{{ cookiecutter.gcs_bucket }}/{{ cookiecutter.gcs_path }}/data/`.
* `make sync_data_from_gcs` will use `gsutil -d -r rsync` to recursively sync files from `gs://{{ cookiecutter.gcs_bucket }}/{{ cookiecutter.gcs_path }}/data/` to `data/`.
