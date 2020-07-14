FROM duffney/ansible:azure

# RUN yum check-update; \
#    yum install -y gcc libffi-devel python-devel openssl-devel epel-release; \
#    yum install -y python-pip python-wheel; \
#    yum install -y openssh-clients; \
#    yum install -y sshpass; \
#    curl https://packages.microsoft.com/config/rhel/7/prod.repo | tee /etc/yum.repos.d/microsoft.repo; \
#    yum install -y powershell; \
#    pwsh -c "Set-PackageSource -Name PSGallery -Trusted"; \
#    pwsh -c "Install-Module AZ -Scope AllUsers"; \
#    pip install --upgrade pip

# RUN  pip install ansible[azure]; \
#    pip install "pywinrm>=0.3.0"

ENV ANSIBLE_HOST_KEY_CHECKING false
ENV ANSIBLE_GATHERING smart
ENV ANSIBLE_RETRY_FILES_ENABLED false

#WORKDIR /ansible

COPY ./entrypoint.sh /entrypoint.sh

ENTRYPOINT ["bash","/entrypoint.sh"]

#ENTRYPOINT ["ansible-playbook","playbook.yml"]