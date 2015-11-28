# ansible-omnios-ips-repository

Creates an IPS repository for OmniOS

usage:


    - hosts: repository
      roles:
      - { role: omnios-ips-repository,
          dataset: DATASET_PATH,
          mount_path: LOCAL_MOUNT_PATH,
          publisher: PUBLISHER }
