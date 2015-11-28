# ansible-omnios-ips-repository

Creates an IPS repository for OmniOS

usage:


    - hosts: repository
      roles:
      - { role: omnios-ips-repository,
          dataset: DATASET_PATH,
          mount_path: LOCAL_MOUNT_PATH,
          depotd_port: PORT,
          publisher: PUBLISHER }

This places a script in `{{LOCAL_MOUNT_PATH}}/scripts` that will configure
depotd as ansible doesn't have great support for SMF yet.
