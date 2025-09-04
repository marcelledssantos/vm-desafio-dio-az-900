Resumo do Desafio – Criação de Máquina Virtual na Azure
Objetivo

O desafio tinha como proposta colocar em prática os conceitos de máquinas virtuais dentro do Azure, passando por todo o processo de criação, configuração e acesso ao recurso.

Passo a passo realizado:

Primeiro foi criado um grupo de recursos para organizar os serviços utilizados. Esse grupo foi chamado de vm-desafio-dio
Em seguida, iniciei a criação da máquina virtual pelo portal do Azure. 

Na tela de configuração, defini os principais parâmetros:
Nome: desafio-vm-dio

Região: East US 2 (ubs2) (mais barata)

Sistema operacional: Ubuntu Server 22.04 LTS

Tamanho: B1s, por ser uma opção de baixo custo

Usuário administrador: azureuser

Método de autenticação: chave SSH

Na etapa de rede, mantive a configuração padrão de criação de IP público e liberei a porta 22 para permitir a conexão via SSH.
Após revisar as configurações, finalizei a criação da máquina virtual. Em poucos minutos ela já estava disponível.
Para acessar a VM, utilizei o arquivo de chave privada que foi gerado durante a configuração. Corrigi as permissões do arquivo no terminal e estabeleci a conexão com o comando:

ssh -i ~/Downloads/desafio-vm-dio_key.pem azureuser@<IP-Publico>


A conexão foi bem-sucedida e pude acessar o ambiente Linux diretamente pelo terminal.

Evidências

Durante o processo, registrei capturas de tela das etapas principais: criação do grupo de recursos, configuração da VM, tela de validação, além da conexão via SSH confirmando que a máquina estava em funcionamento.

Conclusão

A atividade ajudou a reforçar na prática como funciona o provisionamento de máquinas virtuais no Azure. Foi possível entender o papel dos grupos de recursos, a importância de configurar corretamente a rede e a diferença entre os métodos de autenticação. Além disso, ficou mais claro o conceito de infraestrutura como serviço, já que todo o ambiente foi criado sob demanda em poucos minutos.
