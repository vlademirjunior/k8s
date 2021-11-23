Kubernetes é uma plataforma de orquestração de containers.

- Escalonamento automático baseado em politicas de processamento de CPU.
- Healtchecks
- Deploy sem downtime ou minimo possível

Hoje o kubernetes esta hospedado de baixo da CNCF (Cloud Nativa Computiong Foundation), diversos parceiros que contribuem para o desenvolvimento, pode ser rodado em qualquer lugar.

_______________

Cluster = Grupo de servidores que tem um propósito em comum
_______________

Como funciona um Cluster Kubernetes:
Funciona no modelo Master / Slave 
Master: Kubernete Master ou Control Plane (Ele que diz como tudo vai funcionar)
    Componentes:
    - Kube-controller manager
    - Kube-api-server "é o frontend do kubernetes) - Através dele que a gente interage com kubernetes através do kubectl
    - Kube-Scheduler "Verifica o status do cluster kubernetes em toda ação para saber se é possível executar a tarefa desejada"
    - Etcd "onde fica todos os dados e configurações sobre o estado do nosso cluster"
    - Cloud-controller-manager

Slave: Kubernetes Nodes (Recebe as solicitações  de orquestração do master e executa as aplicações)
    Nós: Roda as aplicações
    Componentes:
    - Kubelet "é o agente do kubernetes, um pequeno aplicativo que se comunica com nó master para garantir que sua aplicação esta rodando."
    - Kube-proxy "é um proxy de redes para facilitar os serviços de redes do cluster de dentro e fora"

_________________________________________
Pod = 1 ou mais container em execução
Pod gerencia um contjunto de 1 ou vários containers.
dentro de um pode é executado containers para serem gerenciados como um grupo (deployments)
_____________________________________________________________________________________________