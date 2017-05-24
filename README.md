# ansible-omnios-ips-repository

Creates an IPS repository for OmniOS

usage:


    - hosts: repository
      roles:
      - { role: omnios-ips-repository,
          dataset: DATASET_PATH,
          mount_path: LOCAL_MOUNT_PATH,
          depotd_port: PORT,
          readonly: "true",
          publisher: PUBLISHER }

This places a script in `{{LOCAL_MOUNT_PATH}}/scripts` that will configure
depotd as ansible doesn't have great support for SMF yet.

Setting `readonly` to `false` will allow you to add packages via HTTP.
