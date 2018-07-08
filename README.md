curl -fsSL get.docker.com -o get-docker.sh
sh get-docker.sh
nano /etc/docker/daemon.json

{"insecure-registries": ["172.30.0.0/16"]}

rm -rf /home/oocp/*;

oc cluster up vn --public-hostname=oocp.kynu.xyz --routing-suffix=oocp.kynu.xyz --service-catalog --host-data-dir=/home/oocp/os_data_persisted --use-existing-config;

oc adm config set-credentials vn --username=developer --password=S90851026x;

oc adm config set-credentials vn --username=system --password=S90851026x;
