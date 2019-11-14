# Playbook Collection

[RoleList](https://raw.githubusercontent.com/JollyFellows/portal/master/requirements/hello.yml)

[README.md](../../../../DaithK/hello/blob/master/README.md)

mkdir ansible_work

cd ansible_work/

wget -e"https_proxy=172.22.0.1:58080/" https://raw.githubusercontent.com/JollyFellows/portal/master/requirements/hello.yml

export http_proxy=http://172.22.0.1:58080/

export https_proxy=http://172.22.0.1:58080/

export no_proxy=127.0.0.1,localhost,172.22.0.200,172.22.0.210,172.22.0.220

ansible-galaxy install -r hello.yml -p roles

ansible-playbook -i inventory hello.yml
