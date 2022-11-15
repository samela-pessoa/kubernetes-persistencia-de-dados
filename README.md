# Persistência de dados com pods kubernetes, cloud GCP(Google Cloud Platform).

 > Explicação: pods kurbernetes são efêmeros, com isso caso algum pod seja deletado, os dados contidos nele, também seram perdidos. Para persistência desses dados em casos de falhas ou exclusões de pod, podemos utilizar como base, os recursos e configurações descritas nesse material disponibilizado.

### Requisitos necessários na GCP:

- Criar uma conta.
- Criar um disco.
- Criar um cluster kubernetes.
- Para criação dos pods, executar os arquivos .yaml disponibilizados, no cloud shell.

### baixando os arquivos do repositorio git e executando no cloud shell, para crianção dos pods.
```sh
$git clone https://github.com/samela-pessoa/kubernetes-persistencia-de-dados.git
$cd kubernetes-persistencia-de-dados
$kubectl aplly - f "nomedoarquivo.yaml"
```

### Verificando status do pvc.
```sh
$ kubectl get pvc
```

### Acessando o pod, para verificar o diretorio de persistêcia de dados.
```sh
$ kubectl exec -it pod-pv-1 --container nginx-container  -- bash
$ls
```
