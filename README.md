# Persistência de dados com pods kubernetes no provider GCP

 > Explicação: pods kurbernetes são efemeros, com isso caso algum pod seja deletado, os dados dele também seram perdidos, para que isso não aconteça, realizamos uma configuração para persistência desses dados. 

### Requisitos necessarios:

- Criar uma conta GCP.
- Criar um disco na GCP.
- Criar um cluster na GCP.
- Para criação dos pods, executar os arquivos yaml no cloud shell.

### Acessando o pod, para verificar o diretorio de persistêcia de dados.

```sh
$ kubectl exec -it pod-pv --container nginx-container  -- bash
```