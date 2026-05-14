# solr-k8

O Apache Solr é um servidor de busca open-source, de alta performance, construído sobre a biblioteca Apache Lucene. Ele é projetado para indexar, armazenar e pesquisar grandes volumes de dados (texto completo, estruturados e não estruturados) em tempo real, sendo amplamente utilizado para buscas complexas em sites, e-commerces e aplicações corporativas.

Principais características e funcionalidades:
- **Busca Rápida e Poderosa**: Suporta busca por texto completo, frases exatas, curingas (wildcards), e termos aproximados (fuzzy searches) para corrigir erros de digitação.
- **Recursos Avançados**: Oferece navegação por facetas (filtros), destaque de termos encontrados (highlighting) e autocompletar.
- **Arquitetura REST**: Funciona como um servidor independente que recebe dados e responde a consultas via HTTP, utilizando JSON, XML ou CSV, facilitando a integração com qualquer linguagem de programação.
- **Escalabilidade**: Pronto para produção, suporta computação distribuída, permitindo lidar com volumes massivos de dados.Baseado em Lucene: Utiliza o Lucene no núcleo, garantindo indexação robusta.O Solr é ideal quando se precisa de pesquisas rápidas e inteligentes, sendo usado por empresas como Netflix, CNET e AOL.

[Ref](https://share.google/aimode/dI7zXIyq6e5jxYU7s)

## Sandbox

````
PS C:\Users\rmbarreto> k config current-context
arn:aws:eks:us-east-2:936675601706:cluster/icarros-sandbox-eks-opala
````


````
PS C:\Users\rmbarreto> k get pods --namespace solr
NAME                                 READY   STATUS    RESTARTS   AGE
test-solr-master-865588b777-fnc9x    1/1     Running   0          15d
test-solr-slave-1-75ff4d6b85-g7c2m   1/1     Running   0          7d22h
test-solr-slave-2-8fc67478c-769rn    1/1     Running   0          8d
````

## Prod

````
PS C:\Users\rmbarreto> k config use arn:aws:eks:sa-east-1:480730062915:cluster/prod-eks-gurgel
Switched to context "arn:aws:eks:sa-east-1:480730062915:cluster/prod-eks-gurgel".
````

````
PS C:\Users\rmbarreto> k get pods --namespace solr
NAME                                   READY   STATUS    RESTARTS   AGE
solr-busca-slave1-76cc67c67b-bqkrt     1/1     Running   0          50d
solr-busca-slave2-5b88f966f8-qrprp     1/1     Running   0          50d
solr-busca-slave3-6fd4c98f9b-sc69k     1/1     Running   0          50d
solr-master-65ddc755cd-tsjrg           1/1     Running   0          56d
solr-slave1-6f44c86549-qf6lr           1/1     Running   0          50d
solr-slave10-578c9cf87d-gldhz          1/1     Running   0          50d
solr-slave2-696b56d6c8-bfzcl           1/1     Running   0          50d
solr-slave3-645656bc98-rd9gc           1/1     Running   0          50d
solr-slave4-6b5f447cd8-6t7vs           1/1     Running   0          50d
solr-slave5-b494d7c99-z96sg            1/1     Running   0          50d
solr-slave6-7c7f69957c-nvvgw           1/1     Running   0          50d
solr-slave7-5c9589d98-h2wct            1/1     Running   0          50d
solr-slave8-796c99b796-lqwhc           1/1     Running   0          50d
solr-slave9-699769b648-5fstq           1/1     Running   0          50d
solr-staging-7f66bb96cd-d5p5v          1/1     Running   0          56d
solr-webapp-slave1-5cbb4b6f7b-7zt4p    1/1     Running   0          50d
solr-webapp-slave10-79d9d7988d-xn6fb   1/1     Running   0          50d
solr-webapp-slave2-57d445bc56-xf5xt    1/1     Running   0          50d
solr-webapp-slave3-b9f97f977-z2dqz     1/1     Running   0          50d
solr-webapp-slave4-7b47cbff58-kqzqp    1/1     Running   0          50d
solr-webapp-slave5-54b86f7f5d-qj7zx    1/1     Running   0          50d
solr-webapp-slave6-6b788f469d-lntkk    1/1     Running   0          50d
solr-webapp-slave7-69fd85947d-wz5ds    1/1     Running   0          50d
solr-webapp-slave8-f55fd5dc5-h9ghl     1/1     Running   0          50d
solr-webapp-slave9-5d7b85c74f-sq4m9    1/1     Running   0          50d
````

