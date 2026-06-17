# -CloudFormation
Consolidar seus conhecimentos em tarefas automatizadas com Lambda Function e S3.
aws-cloudformation-lab/
│
├── README.md
├── templates/
│   ├── s3-bucket.yaml
│   ├── ec2-instance.yaml
│   └── network-stack.yaml
│
├── images/
│   ├── stack-created.png
│   ├── s3-created.png
│   └── ec2-created.png
│
└── notes/
    └── aprendizados.md

# Automação de Infraestrutura na AWS com CloudFormation

## Descrição

Este projeto foi desenvolvido como parte do desafio da DIO para praticar conceitos de Infraestrutura como Código (IaC) utilizando AWS CloudFormation.

O objetivo foi criar e gerenciar recursos da AWS através de templates YAML, permitindo a automação do provisionamento de infraestrutura de forma padronizada, escalável e reproduzível.

## Conceitos Praticados

* Infraestrutura como Código (IaC)
* AWS CloudFormation
* Criação de Stacks
* Templates YAML
* Provisionamento de Bucket S3
* Provisionamento de Instância EC2
* Segurança através de Security Groups
* Controle de versão dos templates

## Arquitetura Utilizada

O laboratório foi dividido em três etapas:

### 1. Criação de Bucket S3

Foi criado um bucket S3 utilizando CloudFormation para armazenamento de arquivos.

### 2. Criação de Instância EC2

Foi criada uma instância EC2 utilizando template YAML.

Recursos configurados:

* Amazon Linux
* Tipo t2.micro
* Security Group
* Chave SSH

### 3. Estrutura de Rede

Foram estudados os componentes:

* VPC
* Subnets
* Internet Gateway
* Route Tables

## Template Exemplo – Bucket S3

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: Criacao de Bucket S3

Resources:
  MeuBucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: meu-bucket-cloudformation-lab
```

## Template Exemplo – EC2

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: Criacao de instancia EC2

Resources:
  MinhaInstancia:
    Type: AWS::EC2::Instance
    Properties:
      ImageId: ami-xxxxxxxx
      InstanceType: t2.micro
```

## Como Executar

1. Acesse o CloudFormation no Console AWS.
2. Clique em Create Stack.
3. Faça upload do template YAML.
4. Informe um nome para a Stack.
5. Aguarde a criação dos recursos.

## Evidências

As capturas de tela do laboratório encontram-se na pasta:

```text
/images
```

## Aprendizados

Durante a execução deste laboratório foi possível compreender:

* A importância da automação de infraestrutura.
* Como reduzir erros manuais através de templates.
* A facilidade de replicar ambientes.
* O gerenciamento centralizado dos recursos AWS.
* O conceito de Stack e atualização de recursos.

## Conclusão

O CloudFormation permite gerenciar toda a infraestrutura AWS através de código, facilitando a padronização, escalabilidade e manutenção dos ambientes. O laboratório contribuiu para consolidar conhecimentos em automação e Infraestrutura como Código.
