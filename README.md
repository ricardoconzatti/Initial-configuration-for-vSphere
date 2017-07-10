# Initial configuration for vSphere

Este script utiliza o vSphere PowerCLI para criar um ambiente completo no vSphere, tudo de maneira automatizada e seguindo as recomendações de configurações da VMware. Extremamente recomendado para ambientes de laboratório Nested.

 - **Ações que o Script executa**
	 - Verifica se os hosts ESXi e vCenter Server estão respondendo ping
	 - Conecta no vCenter Server via VMware vSphere PowerCLI
	 - Cria um Data Center
	 - Cria um Cluster
	 - Adiciona os hosts ESXi no Cluster e entra em modo de manutenção
	 - Cria um VDS com dois uplinks e dois Port Groups (Management e vMotion) + a quantidade de Port Groups que você definir
	 - Configura e habilita o vMotion
	 - Migra o VMkernel de gerencia do VSS para o VDS
	 - Remove o VSS
	 - Define o servidor NTP e inicia o serviço
	 - Habilita HA & DRS no Cluster e desabilita o Admission Control (lab only)
	 - Sai do modo de manutenção
	 - Desconecta do vCenter Server
 - **Compatibilidade**
	 - vSphere (ESXi e vCenter)
		 - Testado nas versões 5.1, 5.5, 6.0 e 6.5
	 - PowerCLI
		 - Recomendo a versão 6 ou superior
 - **Pré-requisitos**
	 - vCenter Server (Windows ou Appliance) versão 5 ou superior
	 - Garantir que o vCenter esteja acessivel pela rede
	 - VMware vSphere PowerCLI versão 6 ou superior
	 - 2 ou mais hosts ESXi 6.0 ou superior
		 - Garantir que o ESXi esteja acessível pela rede. Configurar o IP, DNS e hostname
	 - Criar entradas DNS para todos os hosts ESXi e vCenter
		 - Resolução de nomes (curto e FQDN)

[Mais informações](http://solutions4crowds.com.br/script-para-configuracao-inicial-ambiente-vmware-vsphere)
