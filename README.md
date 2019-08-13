# ansible-zabbix-agent
Repositório dedicado para automatização do agent do zabbix, utilizando Ansible.

## Estrutura do repositório:

```
├── main.yml                                >> Chama as tarefas
├── README.md
└── roles                                   >> Estrutura do Ansible
    ├── files                               >> Arquivos/Pacotes
    │   ├── zabbix_agentd.conf
    │   └── zabbix-api-0.5.3.tar.gz
    └── tasks                               >> Tarefas
        ├── agent-zabbix.yml
        └── main.yml                        >> Chama as tarefas
```

## Como utilizar?
Primeiro iremos clonar o repositório.

```
$ git clone git@github.com:gersontpc/ansible-zabbix-agent.git
```
Após clonar o repositório ajuste os parâmetros do playbook e arquivo de configuração com as informações do seu zabbix server, esses arquivos são: zabbix_agentd.conf e agent-zabbix.yml.

## Executando playbook

Ao executar o playbook iremos chamar setar o arquivo main, arquivo que chama as tasks e em extra-vars colocar o grupo ou nome do host que você definiu no seu arquivo de hosts do Ansible.

```
$ cd ansible-zabbix-agent

$ ansible-playbook main.yml --extra-vars "hosts=grupodehosts"
```

Após executar o seu playbook, basta ir no fontend do zabbix e conferir o host lá! ;)  

## Quer fazer alguma melhoria?
Mande um Pull Request :)  

Link para o artigo: [Linux na Web](https://www.linuxnaweb.com/instalacao-automatizada-agente-zabbix-com-ansible/)  
**Créditos:**
Gilberto Guilherme