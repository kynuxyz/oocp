curl -fsSL get.docker.com -o get-docker.sh
sh get-docker.sh
nano /etc/docker/daemon.json

{"insecure-registries": ["172.30.0.0/16"]}

oc cluster up --public-hostname=oocp.kynu.xyz --routing-suffix=oocp.kynu.xyz --service-catalog --host-data-dir=/home/oocp/os_data_persisted --use-existing-config

oadm config set-credentials test --username=developer --password=S90851026x
oadm config set-credentials test --username=system --password=S90851026x
