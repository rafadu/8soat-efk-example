# 8soat-efk-example
Exemplo de instalação de EFK dentro de um cluster Kubernetes, oferecido pelo curso de Arquitetura de Software

# Observações
Arquivos atendem ao cenário de instalação do EFK em um cluster de Kubernetes com as seguintes configurações:
- Máquina Virtual com Ubuntu Server 22.04.3
- MicroK8s como serviço de Kubernetes

Os arquivos seguem o exemplo do vídeo, onde a rota do Kibana está configurada para a porta 30000 e a do Elastic para a 31300.
No exemplo da Aula, é utilizada a versão 7.5.0 do Kibana, neste repositório foi necessário usar a versão 7.2.0 por um erro causado por diferença entre a versão do Kibana e a versão do ElasticSearch.
Na aula não cita a necessidade de configurar um StorageClass, nem um PersistentVolume. Sem eles não será possível vincular o Volume utilizado pelo ElasticSearch

# Instalação

Baixe este repositório em um caminho acessível pelo seu cluster de Kubernetes
Execute os arquivos via o comando "kubectl apply -f <nome do arquivo>"
Ideal executar primeiro o arquivo storage.yml antes dos outros, depois não há necessidade de seguir uma ordem. Porem para que o Kibana funcione, é necessário que ElasticSearch e FluentD estejam instalados primeiro
