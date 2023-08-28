

# deploy logstash config and restart
sudo ansible-playbook --ask-vault-pass -i inventory/pro/hosts.ini playbooks/deploy_pipeline.yml -k

# Deploy main pipeline and restart
sudo ansible-playbook --ask-vault-pass -i inventory/pro/hosts.ini playbooks/deploy_logstash_pipeline.yml -k

# Create vaults
ansible-vault create secret.yml

