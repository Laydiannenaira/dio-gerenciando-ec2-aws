# Desafio de Gerenciamento de Instâncias EC2 na AWS

**Autor:** Laydianne Costa

**Projeto:** Conclusão do desafio de laboratório da Formação AWS Cloud Foundations, com foco em Gerenciamento de Instâncias EC2.

---

## 1. Introdução: O Que é EC2?

O Amazon Elastic Compute Cloud (EC2) é um serviço da AWS que nos fornece a capacidade de computação na nuvem, atuando como máquinas virtuais com sistemas operacionais Windows ou Linux.

Uma instância EC2 é composta por diversos recursos, como:

- **CPU**
- **Memória**
- **Disco**
- **Rede**
- **Sistema Operacional**

No modelo de nuvem, o EC2 é um exemplo de **Infraestrutura como Serviço (IaaS)**. Isso significa que, ao usar esse serviço, nossa responsabilidade se concentra em gerenciar os aplicativos, dados e as conexões que estabelecemos com a instância.

---

## 2. Passo a Passo do Projeto

### 2.1. Criação e Execução da Instância

O primeiro passo foi provisionar uma instância EC2. A tela abaixo confirma que a instância foi criada com sucesso e está em estado de execução (`running`).

![Visão Geral da Instância EC2](images/instanciacriada.png)

A escolha da instância correta é crucial para garantir a eficiência e a economia. Para este projeto, foi utilizada uma instância do tipo `t2.nano`, adequada para tarefas de desenvolvimento e testes.

![Detalhes da Instância EC2](images/instanciadetalhes.png)

### 2.2. Configuração de Segurança (Grupo de Segurança)

Para proteger a instância, utilizei um **Grupo de Segurança**, que funciona como um firewall embutido na AWS. Ele permite controlar o tráfego de rede para a instância.

A imagem a seguir mostra as regras de entrada (`Inbound Rules`) que configurei, permitindo o acesso via SSH (porta 22), que é essencial para o gerenciamento remoto da máquina.

![Regras de Entrada do Grupo de Segurança](images/instancia-seguranca.png)

### 2.3. Otimização de Custos

Um dos princípios fundamentais da nuvem é a otimização de recursos, que está diretamente ligada à economia de custos[cite: 2]. Desligar recursos não utilizados em ambientes de desenvolvimento, teste ou treinamento é uma das principais formas de poupar gastos, já que a cobrança é baseada no tempo de execução[cite: 2].

Como demonstrado abaixo, a instância foi parada (`stopping`). Ao parar a instância, os recursos de CPU, memória e rede são desativados, e a cobrança é suspensa.grupo-de-seguranca

![Instância EC2 parada](images/instancia-parada.png)

---

## 3. Conclusão e Aprendizados

Este desafio me permitiu aplicar, na prática, os conceitos teóricos sobre EC2 e gerenciamento de nuvem. Através deste exercício, pude entender a importância de:

- Escolher o tipo de instância correto para a workload.
- Configurar regras de segurança para proteger o ambiente.
- Otimizar recursos para evitar custos desnecessários.

Este projeto no GitHub serve como um portfólio técnico e um material de apoio para revisões futuras.
