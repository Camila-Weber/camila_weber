# Camila Weber - Engenharia de Software
---

Disciplina: Engenharia de Software

Discente: Camila Weber

Docente: Emiliano Soares Monteiro

- [Camila Weber - Engenharia de Software](#camila-weber---engenharia-de-software)
- [1. Introdução](#1-introdução)
- [2. Descrição do negócio](#2-descrição-do-negócio)
- [3. Visão geral do sistema](#3-visão-geral-do-sistema)
  - [3.1. Principais Módulos do Sistema](#31-principais-módulos-do-sistema)
  - [3.2. O que o Sistema Entrega do Ponto de Vista do Usuário Final](#32-o-que-o-sistema-entrega-do-ponto-de-vista-do-usuário-final)
- [4. Diagrama ER](#4-diagrama-er)
  - [4.1. Descrição das Entidades](#41-descrição-das-entidades)
- [5. Diagrama de classe](#5-diagrama-de-classe)
  - [5.1. Descrição das Classes](#51-descrição-das-classes)
- [6. Casos de uso](#6-casos-de-uso)
  - [6.1. Casos de uso](#61-casos-de-uso)
  - [6.2. Histórias de usuários](#62-histórias-de-usuários)
    - [6.2.1. Cadastro de Cliente e Animal](#621-cadastro-de-cliente-e-animal)
    - [6.2.2. Marcação de Atendimento](#622-marcação-de-atendimento)
    - [6.2.3. Registro de Condições](#623-registro-de-condições)
    - [6.2.4. Atendimento de Emergência](#624-atendimento-de-emergência)
    - [6.2.5. Receitas e Orientações](#625-receitas-e-orientações)
    - [6.2.6. Ficha e Prontuário do Animal](#626-ficha-e-prontuário-do-animal)
    - [6.2.7. Agendamento de Hospedagem](#627-agendamento-de-hospedagem)
    - [6.2.8. Serviços de Banho e Tosa](#628-serviços-de-banho-e-tosa)
    - [6.2.9. Creche para Animais](#629-creche-para-animais)
    - [6.2.10. Compras no Petshop](#6210-compras-no-petshop)
    - [6.2.11. Pagamento das Contas](#6211-pagamento-das-contas)
- [7. Diagrama de componentes](#7-diagrama-de-componentes)
- [8. Diagrama de Implantação](#8-diagrama-de-implantação)
- [9. Protótipo de telas](#9-protótipo-de-telas)
  - [9.1. Tela de Login](#91-tela-de-login)
  - [9.2. Tela de Menu/Abertura](#92-tela-de-menuabertura)
  - [9.3. Tela de Relatório de Clientes](#93-tela-de-relatório-de-clientes)
  - [9.4. Tela de Relatório de Animais](#94-tela-de-relatório-de-animais)
  - [9.5. Tela de Relatório de Veterinários](#95-tela-de-relatório-de-veterinários)
  - [9.6. Tela de Relatório de Hospedagem](#96-tela-de-relatório-de-hospedagem)
  - [9.7. Tela de Relatório de Internação](#97-tela-de-relatório-de-internação)
  - [9.8. Tela de Relatório de Produto](#98-tela-de-relatório-de-produto)
  - [9.9. Tela de Relatório de Creche](#99-tela-de-relatório-de-creche)
  - [9.10. Tela de Relatório de Pagamento](#910-tela-de-relatório-de-pagamento)
  - [9.11. Tela de Relatório de Atendimento](#911-tela-de-relatório-de-atendimento)
  - [9.12. Tela de Gráfico](#912-tela-de-gráfico)
    - [9.12.1. Gráfico Preço dos Produtos](#9121-gráfico-preço-dos-produtos)
  - [9.13. Tela de Dashboard](#913-tela-de-dashboard)
- [10. Diagrama de navegação de telas](#10-diagrama-de-navegação-de-telas)
- [11. Pilha tecnológica](#11-pilha-tecnológica)
- [12. Requisitos de sistemas](#12-requisitos-de-sistemas)
  - [12.1. Requisitos do Cliente](#121-requisitos-do-cliente)
  - [12.2. Requisitos do Servidor](#122-requisitos-do-servidor)
- [13. Considerações sobre segurança](#13-considerações-sobre-segurança)
  - [13.1. Lado Cliente](#131-lado-cliente)
  - [13.2. Lado Servidor](#132-lado-servidor)
- [14. Manutenção, Instalação e Novas Funcionalidades](#14-manutenção-instalação-e-novas-funcionalidades)
  - [14.1. Manutenção](#141-manutenção)
  - [14.2. Instalação](#142-instalação)
  - [14.3. Novas Funcionalidades](#143-novas-funcionalidades)
- [15. Treinamento](#15-treinamento)
  - [15.1. Usuário](#151-usuário)
  - [15.2. Administrador do Sistema](#152-administrador-do-sistema)
- [16. Script SQL](#16-script-sql)
  - [16.1. Comandos CREATE table](#161-comandos-create-table)
  - [16.2. Comandos INSERT gerando dados fictícios](#162-comandos-insert-gerando-dados-fictícios)

---
# 1. Introdução

O projeto a seguir apresenta um sistema desenvolvido para um petshop. A empresa é considerada micro e iniciou as atividades recentemente. Ao possuir serviços excluvivos, os sistemas presentes no mercado não se enquadram, desta forma, os proprietários decidiram desenvolver uma solução própria. Esta solução é detalhada a seguir:

---
# 2. Descrição do negócio

Descrição do cenário onde o sistema deverá funcionar:

**1.** Uma clínica veterinária atende apenas os animais: gatos e cachorros.

**2.** Marcar os animais RFID, a pedido do cliente.

**3.** Os clientes devem fazer um cadastro de si, contendo informações pessoais e de contato, e dos animais, como nome e descrições.

**4.** Os clientes devem informar as condições nas quais os animais chegam, para atendimentos com o veterinário, informar se o atendimento é de rotina ou de emergência.

**5.** Os clientes devem informar o tipo de ração que o animal come e se existe alguma condição médica que possa afetar o atendimento.

**6.** O cliente deve informar hábitos do animal.

**7.** Para cada animal é possível que mais de um veterinário o atenda, e um veterinário pode atender mais de um animal.

**8.** Os animais podem chegar e serem atendidos de acordo com uma agenda do dia.

**9.** Os clientes podem marcar um horário com antecedência, podendo escolher o veterinário e não enfrentar filas de atendimento.

**10.** Cada animal atendido receberá uma ficha, contendo as informações de cadastro e outras adicionais, e um prontuário, com registros de consultas, procedimentos e condições médicas.

**11.** Quando necessário o atendimento gera uma receita para o animal, com informações sobre medicamentos, dosagens e horários, além de outras orientações.

**12.** Quando um cliente chega na clínica veterinária ele é atendido por um atendente, que irá efetuar o cadastro do cliente e do animal, caso não esteja no sistema.

**13.** O atendente deve verificar se existe agenda disponível com um veterinário e preencher o horário, se disponível.

**14.** O atendente deve colocar o cliente e seu animal na fila de espera, se for o caso.

**15.** O atendente deve levar o cliente e o animal até o veterinário.

**16.** O veterinário deve realizar uma entrevista com o dono do animal.

**17.** O resultado da entrevista deve ir para um formulário.

**18.** O veterinário deverá examinar o animal e anotar em prontuário(ficha) suas observações.

**19.** Dependendo da situação do animal este receberá uma receita.

**20.** A clínica faz atendimentos médicos de emergência, como cirurgias e curativos para machucados.

**21.** A clínica possui alguns veterinários de plantão durante a madrugada, ficando aberta 24 horas.

**22.** O veterinário pode aplicar vacinas de acordo com o pedido do cliente ou da situação.

**23.** Os atendimentos e as vacinas são agendadas, a não ser em caso de emergência grave, onde um médico de plantão irá atender o animal.

**24.** A clínica oferece serviços de hospedagem, em casos de que o cliente viaje e queira deixar o animal aos cuidados da clínica.

**25.** Para usufruir da hospedagem o cliente tem que agendar a data com pelo menos uma semana de antecedência e informar a data de retorno.

**26.** Durante o período de hospedagem, os animais receberam alimentação e cuidados, além de brincadeiras e caminhadas, tudo supervisionado por funcionários treinados.

**27.** A clínica também oferece a internação, em casos de saúde ou procedimentos cirúrgicos e médicos.

**28.** A clínica conta com uma equipe especializada em cuidados animais, fornecendo banho e tosa, sob agendamento.

**29.** A clínica conta com ambientes de creche, nos quais os animais podem passar o dia sendo supervisionados por funcionarios treinados, são disponibilizados planos mensais/diários para a creche.

**30.** O petshop tem um grande estoque de produtos de higiene, brinquedos e rações das melhores marcas a venda para os clientes.

**31.** O petshop tem parceria com farmácias e oferece descontos para clientes que possuem cadastro.

**32.** O pagamento das da conta pode ser feito em dinheiro, pix e cartões.

---
# 3. Visão geral do sistema

O sistema proposto para a clínica veterinária é uma plataforma abrangente que integra diversas funcionalidades voltadas ao atendimento e ao gerenciamento de animais, clientes e serviços. Ele permite o cadastro de clientes e seus animais, agendamento de consultas, gestão de prontuários, geração de receitas, além de oferecer serviços adicionais como hospedagem, internação e creche.

## 3.1. Principais Módulos do Sistema

- Cadastro de Clientes e Animais: Os usuários podem criar perfis que contêm informações pessoais e dados dos animais, incluindo histórico de saúde e preferências alimentares.

- Agendamento: Permite que os clientes marquem atendimentos com veterinários, escolhendo horários e serviços conforme a necessidade (rotina ou emergência).

- Atendimento Veterinário: Inclui a realização de entrevistas, exames e anotações em prontuário, além da geração de receitas e orientações pós-atendimento.

- Serviços Adicionais: Gerencia a hospedagem, internação, banho e tosa, e creche, proporcionando uma experiência completa para os animais sob cuidados.

- Venda de Produtos: Integra um petshop com um amplo estoque de produtos, permitindo que os clientes façam compras diretamente na clínica.

- Pagamentos: Oferece opções variadas de pagamento, incluindo dinheiro, pix e cartões, facilitando a transação.

## 3.2. O que o Sistema Entrega do Ponto de Vista do Usuário Final

- Acesso Rápido a Serviços: O sistema oferece uma interface amigável que permite aos clientes agendar consultas e serviços de forma eficiente e intuitiva.

- Atendimento Personalizado: Cada animal é tratado de forma única, com informações detalhadas coletadas e registradas, o que resulta em um atendimento mais adequado às suas necessidades.

- Histórico Completo de Saúde: Os clientes têm acesso a prontuários completos, que documentam todas as consultas, tratamentos e observações, permitindo um acompanhamento contínuo da saúde dos animais.

- Flexibilidade de Agendamento: A possibilidade de agendar atendimentos com antecedência, escolhendo veterinários e horários, proporciona comodidade e evita filas.

- Serviços de Emergência: O sistema garante atendimento imediato em situações de emergência, com veterinários disponíveis 24 horas, assegurando cuidados urgentes quando necessário.

- Cuidado e Conforto Durante a Hospedagem: Clientes podem agendar a hospedagem de seus animais, com a certeza de que receberão cuidados adequados, alimentação e atividades recreativas.

- Facilidade de Compras: A integração com o petshop permite que os clientes adquiram produtos essenciais durante suas visitas, simplificando o processo de compra.

- Descontos e Benefícios: O sistema oferece acesso a descontos em farmácias para clientes cadastrados, proporcionando vantagens adicionais.

- Variedade nos Métodos de Pagamento: A aceitação de diferentes formas de pagamento garante que os clientes possam realizar transações de forma prática e conveniente.

- Experiência Geral Positiva: A combinação de funcionalidades robustas e uma interface amigável resulta em uma experiência de usuário satisfatória, fortalecendo a relação entre a clínica e seus clientes.

Esses elementos destacam como o sistema atende às necessidades dos usuários finais, promovendo uma gestão eficiente e um atendimento de qualidade na clínica veterinária.

---
# 4. Diagrama ER

```mermaid
erDiagram
    CLIENTE {
        string id_cliente PK
        string nome
        string cpf
        string telefone
        string email
    }

    ANIMAL {
        string id_animal PK
        string nome
        string tipo 
        string descricao
        string condicao_medica
        string tipo_racao
        string habitos
        string rfid
    }
    
    VETERINARIO {
        string id_veterinario PK
        string nome
        string especializacao
        string plantao
    }
    
    ATENDIMENTO {
        string id_atendimento PK
        string id_cliente FK
        string id_animal FK
        string id_veterinario FK
        string data_hora
        string tipo_atendimento 
        string formulario
        string prontuario
        string receita
    }
    
    HOSPEDAGEM {
        string id_hospedagem PK
        string id_cliente FK
        string id_animal FK
        date data_inicio
        date data_fim
        string cuidados
    }
    
    INTERNACAO {
        string id_internacao PK
        string id_cliente FK
        string id_animal FK
        string motivo
        date data_inicio
        date data_fim
    }
    
    CRECHE {
        string id_creche PK
        string id_animal FK
        date data
        string plano
    }
    
    PRODUTO {
        string id_produto PK
        string nome
        string categoria
        float preco
        string descricao
    }
    
    PAGAMENTO {
        string id_pagamento PK
        string id_cliente FK
        float valor
        string metodo_pagamento 
        date data_pagamento
    }

    CLIENTE ||--o{ ANIMAL : possui
    CLIENTE ||--o{ ATENDIMENTO : realiza
    CLIENTE ||--o{ HOSPEDAGEM : agenda
    CLIENTE ||--o{ INTERNACAO : solicita
    CLIENTE ||--o{ PAGAMENTO : efetua
    ANIMAL ||--o{ ATENDIMENTO : participa
    ANIMAL ||--o{ HOSPEDAGEM : se_hospeda
    ANIMAL ||--o{ INTERNACAO : se_interna
    ANIMAL ||--o{ CRECHE : frequenta
    VETERINARIO ||--o{ ATENDIMENTO : atende
    ATENDIMENTO ||--o{ PRODUTO : inclui
```

## 4.1. Descrição das Entidades

> **CLIENTE**: Representa os clientes da clínica, incluindo informações pessoais e de contato.
> 
> **ANIMAL**: Registra os animais cadastrados, com detalhes sobre nome, tipo, condições médicas e hábitos.
> 
> **VETERINARIO**: Contém informações sobre os veterinários, incluindo especializações e horários de plantão.
> 
> **ATENDIMENTO**: Relaciona os atendimentos realizados, incluindo informações sobre o cliente, animal, veterinário, tipo de atendimento e documentação gerada (prontuário, receita).
> 
> **HOSPEDAGEM**: Informações sobre os períodos em que os animais ficam hospedados na clínica.
> 
> **INTERNAÇÃO**: Registra informações sobre internações de animais, incluindo motivos e períodos.
> 
> **CRECHE**: Detalha as atividades e planos para animais que frequentam a creche da clínica.
> 
> **PRODUTO**: Representa os produtos disponíveis para venda na clínica.
> 
> **PAGAMENTO**: Contém informações sobre os pagamentos realizados pelos clientes.


---
# 5. Diagrama de classe

```mermaid
classDiagram
    class Cliente {
        +int id_cliente
        +String nome
        +String cpf
        +String telefone
        +String email
        +List<Animal> animais
        +cadastrar()
    }

    class Animal {
        +int id_animal
        +String nome
        +String tipo
        +String descricao
        +String condicao_medica
        +String tipo_racao
        +String habitos
        +String rfid
        +List<Veterinario> veterinarios
        +atender()
    }

    class Veterinario {
        +int id_veterinario
        +String nome
        +String especializacao
        +boolean plantao
        +List<Animal> atendimentos
        +atenderAnimal()
        +aplicarVacina()
    }

    class Atendimento {
        +int id_atendimento
        +Date data_hora
        +String tipo_atendimento
        +String formulario
        +String prontuario
        +String receita
        +Cliente cliente
        +Animal animal
        +Veterinario veterinario
        +registrar()
    }

    class Hospedagem {
        +int id_hospedagem
        +Date data_inicio
        +Date data_fim
        +String cuidados
        +Animal animal
    }

    class Internacao {
        +int id_internacao
        +String motivo
        +Date data_inicio
        +Date data_fim
        +Animal animal
    }

    class Creche {
        +int id_creche
        +Date data
        +String plano
        +Animal animal
    }

    class Produto {
        +int id_produto
        +String nome
        +String categoria
        +double preco
        +String descricao
    }

    class Pagamento {
        +int id_pagamento
        +double valor
        +String metodo_pagamento
        +Cliente cliente
    }

    Cliente "1" -- "0..*" Animal : possui
    Veterinario "1" -- "0..*" Atendimento : atende
    Animal "0..*" -- "0..*" Veterinario : é atendido por
    Atendimento "1" -- "1" Cliente : registra
    Atendimento "1" -- "1" Animal : inclui
    Atendimento "1" -- "1" Veterinario : gerado por
    Animal "0..*" -- "0..*" Hospedagem : se hospeda
    Animal "0..*" -- "0..*" Internacao : se interna
    Animal "0..*" -- "0..*" Creche : frequenta
    Cliente "1" -- "0..*" Pagamento : realiza
```

## 5.1. Descrição das Classes

> **Cliente**: Representa os clientes da clínica, com métodos para cadastrar clientes e gerenciar seus animais.
> 
> **Animal**: Contém informações sobre os animais, como tipo e descrição, e métodos para gerenciar atendimentos.
> 
> **Veterinario**: Armazena dados sobre os veterinários e seus métodos de atendimento e aplicação de vacinas.
> 
> **Atendimento**: Registra informações sobre os atendimentos realizados, incluindo clientes, animais e veterinários.
> 
> **Hospedagem**: Representa serviços de hospedagem para animais.
> 
> **Internacao**: Armazena informações sobre internações de animais.
> 
> **Creche**: Detalha atividades dos animais na creche.
> 
> **Produto**: Representa os produtos disponíveis para venda na clínica.
> 
> **Pagamento**: Armazena informações sobre os pagamentos realizados pelos clientes.

---
# 6. Casos de uso

## 6.1. Casos de uso

![Figura 1 - Casos de uso](https://github.com/Camila-Weber/camila_weber/blob/main/telas/casos_de_uso.png)

## 6.2. Histórias de usuários

### 6.2.1. Cadastro de Cliente e Animal

> **Como** um cliente,  
> **quero** cadastrar minhas informações e as do meu animal,  
> **para** que eu possa agendar atendimentos e receber cuidados adequados.


### 6.2.2. Marcação de Atendimento

> **Como** um cliente,  
> **quero** marcar um horário com antecedência,  
> **para** que eu possa escolher o veterinário e evitar filas.

### 6.2.3. Registro de Condições

> **Como** um cliente,  
> **quero** informar as condições de saúde do meu animal e seus hábitos,  
> **para** que o veterinário possa oferecer um atendimento adequado.

### 6.2.4. Atendimento de Emergência

> **Como** um cliente,  
> **quero** saber que posso levar meu animal para atendimento de emergência a qualquer hora,  
> **para** que ele receba os cuidados necessários rapidamente.

### 6.2.5. Receitas e Orientações

> **Como** um veterinário,  
> **quero** gerar receitas com informações detalhadas após o atendimento,  
> **para** que os clientes possam seguir corretamente as orientações de cuidado.

### 6.2.6. Ficha e Prontuário do Animal

> **Como** um veterinário,  
> **quero** registrar todas as informações e observações em uma ficha,  
> **para** que haja um histórico completo do atendimento do animal.

### 6.2.7. Agendamento de Hospedagem

> **Como** um cliente,  
> **quero** agendar a hospedagem do meu animal com uma semana de antecedência,  
> **para** que eu possa viajar tranquilo, sabendo que ele está bem cuidado.

### 6.2.8. Serviços de Banho e Tosa

> **Como** um cliente,  
> **quero** agendar serviços de banho e tosa,  
> **para** que meu animal possa ficar limpo e bem cuidado.

### 6.2.9. Creche para Animais

> **Como** um cliente,  
> **quero** inscrever meu animal na creche,  
> **para** que ele tenha companhia e cuidados durante o dia.

### 6.2.10. Compras no Petshop

> **Como** um cliente,  
> **quero** comprar produtos de higiene e ração no petshop da clínica,  
> **para** que eu possa encontrar tudo o que preciso em um só lugar.

### 6.2.11. Pagamento das Contas

> **Como** um cliente,  
> **quero** ter opções de pagamento como dinheiro, pix e cartões,  
> **para** que eu possa escolher a forma que for mais conveniente para mim.

---
# 7. Diagrama de componentes

![Figura 19 - Protótipo da Tela de Login](https://github.com/Camila-Weber/camila_weber/blob/main/telas/diagrama_de_componentes.png)

---
# 8. Diagrama de Implantação

![Figura 20 - Protótipo da Tela de Login](https://github.com/Camila-Weber/camila_weber/blob/main/telas/diagrama_de_implantacao.png)

---
# 9. Protótipo de telas

## 9.1. Tela de Login

![Figura 2 - Protótipo da Tela de Login](https://github.com/Camila-Weber/camila_weber/blob/main/telas/image.png)

## 9.2. Tela de Menu/Abertura

![Figura 3 - Protótipo da Tela de Menu/Abertura](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_menu.jpg)

## 9.3. Tela de Relatório de Clientes

![Figura 4 - Protótipo da Tela de Relatório de Clientes](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grid_cliente.jpg)

## 9.4. Tela de Relatório de Animais

![Figura 5 - Protótipo da Tela de Relatório de Animais](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grid_animal.jpg)

![Figura 6 - Protótipo da Tela de Relatório de Animais](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grid_animal2.jpg)

## 9.5. Tela de Relatório de Veterinários

![Figura 7 - Protótipo da Tela de Relatório de Veterinários](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grid_vet.jpg)

## 9.6. Tela de Relatório de Hospedagem

![Figura 8 - Protótipo da Tela de Relatório de Hospedagem](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grid_hospedagem.jpg)

## 9.7. Tela de Relatório de Internação

![Figura 9 - Protótipo da Tela de Relatório de Internação](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grid_internacao.jpg)

## 9.8. Tela de Relatório de Produto

![Figura 10 - Protótipo da Tela de Relatório de Produto](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grid_produto.jpg)

## 9.9. Tela de Relatório de Creche

![Figura 11 - Protótipo da Tela de Relatório de Creche](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grid_creche.jpg)

## 9.10. Tela de Relatório de Pagamento

![Figura 12 - Protótipo da Tela de Relatório de Pagamento](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grid_pagamento.jpg)

## 9.11. Tela de Relatório de Atendimento

![Figura 13 - Protótipo da Tela de Relatório de Atendimento](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grid_atendimento.jpg)

## 9.12. Tela de Gráfico

### 9.12.1. Gráfico Preço dos Produtos

![Figura 14 - Protótipo da Tela de Gráfico - Preço dos Produtos](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grafico2.jpg)

![Figura 15 - Protótipo da Tela de Gráfico - Preço dos Produtos](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_grafico.jpg)

## 9.13. Tela de Dashboard

![Figura 16 - Protótipo da Tela de Dashboard](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_dashboard.jpg)

![Figura 17 - Protótipo da Tela de Dashboard](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_dashboard2.jpg)

![Figura 18 - Protótipo da Tela de Dashboard](https://github.com/Camila-Weber/camila_weber/blob/main/telas/tela_dashboard3.jpg)

---
# 10. Diagrama de navegação de telas

```mermaid
graph TD
    A[Login] --> B[Menu]
    
    B --> C[Cadastrar Cliente]
    B --> D[Cadastrar Animal]
    B --> E[Agendar Atendimento]
    B --> F[Atendimento Veterinário]
    B --> G[Prontuário]
    B --> H[Receitas Médicas]
    B --> I[Hospedagem]
    B --> J[Internação]
    B --> K[Banho e Tosa]
    B --> L[Creche]
    B --> M[Petshop]
    B --> N[Pagamento]
    
    C --> O[Formulário de Cadastro]
    D --> P[Formulário de Cadastro de Animal]
    E --> Q[Selecionar Veterinário]
    E --> R[Escolher Data e Hora]
    
    F --> S[Entrevista]
    F --> T[Exame do Animal]
    F --> U[Aplicar Vacina]
    
    I --> V[Agendar Hospedagem]
    J --> W[Registrar Internação]
    K --> X[Agendar Banho/Tosa]
    L --> Y[Planos de Creche]
    M --> Z[Consultar Estoque]
    N --> AA[Realizar Pagamento]
```

---
# 11. Pilha tecnológica

```mermaid
graph TD
    A[Camada de Apresentação] --> B[Interface do Usuário]
    A --> C[Aplicativo Web/Móvel]
    
    B --> D[HTML/CSS/JavaScript]
    C --> D

    D --> E[Frameworks]
    
    E --> F[API REST]
    
    F --> G[Camada de Lógica de Negócio]
    
    G --> H[Servidor de Aplicação]
    G --> I[Processamento de Dados]
    
    H --> J[Banco de Dados]
    
    J --> K[PostgreSQL/MySQL]
    
    J --> L[Armazenamento de Documentos]
    
    K --> M[Serviço de Autenticação]
    
    M --> N[OAuth2/JWT]
    
    O[Camada de Integração] --> P[Serviços Externos]
    
    P --> Q[Integração com Petshop]
    P --> R[Parcerias com Farmácias]

    S[Infraestrutura] --> T[Nuvem]
    S --> U[Servidores Físicos/Locais]
```

---
# 12. Requisitos de sistemas

<!-- complementar -->

## 12.1. Requisitos do Cliente

Para que o cliente tenha acesso a aplicação e consiga usar de maneira adequada ele irá precisar:

**1.** Navegadores para acessar a aplicação (Chrome, Firefox, Safari, Edge);

**2.** Endereço de acesso da aplicação;

**3.** Conhecimento do funcionamento do sistema/aplicação;

**4.** Autenticação de Usuário;

## 12.2. Requisitos do Servidor

<!-- Para que a aplicação funcione é necessário que os seguintes requisitos sejam atendidos:

Servidores: Utilizar Apache ou Nginx para servir a aplicação.
Ambiente de Execução: PHP (versão compatível com Scriptcase).
Banco de Dados

SGBD: MySQL ou PostgreSQL como sistema de gerenciamento de banco de dados.
Conexão Segura: Utilizar conexões seguras (SSL) para interações com o banco de dados.
API de Comunicação

Implementar uma API RESTful para permitir a comunicação entre o front-end e o back-end.
Documentação da API para facilitar a integração.
Segurança

Implementar medidas de segurança (firewalls, proteção contra SQL injection, XSS).
Criptografia de dados sensíveis, como senhas (ex.: bcrypt).
Escalabilidade

Capacidade de escalar horizontalmente (adicionando mais servidores) ou verticalmente (aumentando recursos do servidor).
Ambiente de Desenvolvimento e Produção

Configuração de ambientes distintos para desenvolvimento, teste e produção.
Uso de ferramentas de versionamento (ex.: Git).
Monitoramento e Backup

Implementar soluções de monitoramento de servidor e aplicação.
Rotinas de backup regular do banco de dados e arquivos da aplicação.
Integração com Serviços Externos

APIs para integração com serviços de pagamento, petshops, ou outros sistemas necessários. -->

**1.** Componentes da aplicação

**2.** Servidor de Banco de Dados

**3.** Servidor Web

**4.** Banco de Dados

---
# 13. Considerações sobre segurança

## 13.1. Lado Cliente

<!-- regras de senhas
captcha, qtd min. caracteres, maiusculas, minusculas, ...
auteticação de dois fatores
recuperação de senha com email
código no email
anti-virus
mini politica de segurança
CLAUDE
SAPIENS -->


## 13.2. Lado Servidor

<!-- 
politica de backup de aplcação e banco  (1x/mes 1 full backup) (1x por semana um backup incremental)
o admin do sistema não acessa dados do usuario
se for linux não precisa de anti-vírus, outros sim
-->

---
# 14. Manutenção, Instalação e Novas Funcionalidades

## 14.1. Manutenção
<!-- manter o software funcionando -->

## 14.2. Instalação
<!-- instalado no servidor -->

## 14.3. Novas Funcionalidades
<!-- formalizar pedido do cliente
cliente não dá palpite em beleza de tela
decidir sobre 3 critérios:
a) equipe tem tempo?
b) é economicamente viável?
c) é tecnologicamente viável? -->

---
# 15. Treinamento

## 15.1. Usuário

<!-- video na web -->

## 15.2. Administrador do Sistema
<!-- o que vai ser passado para as pessoas reponsaveis/usuarios do sistema -->

---
# 16. Script SQL

## 16.1. Comandos CREATE table

```SQL
-- Tabela de Clientes
CREATE TABLE Cliente (
    id_cliente INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    cpf VARCHAR(11) UNIQUE NOT NULL,
    telefone VARCHAR(15),
    email VARCHAR(100),
    data_cadastro TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Tabela de Animais
CREATE TABLE Animal (
    id_animal INT AUTO_INCREMENT PRIMARY KEY,
    id_cliente INT,
    nome VARCHAR(100) NOT NULL,
    tipo ENUM('gato', 'cachorro') NOT NULL,
    descricao TEXT,
    condicao_medica TEXT,
    tipo_racao VARCHAR(100),
    habitos TEXT,
    rfid VARCHAR(100) UNIQUE,
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id_cliente) ON DELETE CASCADE
);

-- Tabela de Veterinários
CREATE TABLE Veterinario (
    id_veterinario INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    especializacao VARCHAR(100),
    plantao BOOLEAN DEFAULT FALSE
);

-- Tabela de Atendimentos
CREATE TABLE Atendimento (
    id_atendimento INT AUTO_INCREMENT PRIMARY KEY,
    id_cliente INT,
    id_animal INT,
    id_veterinario INT,
    data_hora DATETIME NOT NULL,
    tipo_atendimento ENUM('rotina', 'emergencia') NOT NULL,
    formulario TEXT,
    prontuario TEXT,
    receita TEXT,
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id_cliente) ON DELETE CASCADE,
    FOREIGN KEY (id_animal) REFERENCES Animal(id_animal) ON DELETE CASCADE,
    FOREIGN KEY (id_veterinario) REFERENCES Veterinario(id_veterinario) ON DELETE SET NULL
);

-- Tabela de Hospedagem
CREATE TABLE Hospedagem (
    id_hospedagem INT AUTO_INCREMENT PRIMARY KEY,
    id_cliente INT,
    id_animal INT,
    data_inicio DATE NOT NULL,
    data_fim DATE NOT NULL,
    cuidados TEXT,
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id_cliente) ON DELETE CASCADE,
    FOREIGN KEY (id_animal) REFERENCES Animal(id_animal) ON DELETE CASCADE
);

-- Tabela de Internações
CREATE TABLE Internacao (
    id_internacao INT AUTO_INCREMENT PRIMARY KEY,
    id_cliente INT,
    id_animal INT,
    motivo TEXT,
    data_inicio DATE NOT NULL,
    data_fim DATE NOT NULL,
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id_cliente) ON DELETE CASCADE,
    FOREIGN KEY (id_animal) REFERENCES Animal(id_animal) ON DELETE CASCADE
);

-- Tabela de Creche
CREATE TABLE Creche (
    id_creche INT AUTO_INCREMENT PRIMARY KEY,
    id_animal INT,
    data DATE NOT NULL,
    plano VARCHAR(100),
    FOREIGN KEY (id_animal) REFERENCES Animal(id_animal) ON DELETE CASCADE
);

-- Tabela de Produtos
CREATE TABLE Produto (
    id_produto INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    categoria VARCHAR(100),
    preco DECIMAL(10, 2) NOT NULL,
    descricao TEXT
);

-- Tabela de Pagamentos
CREATE TABLE Pagamento (
    id_pagamento INT AUTO_INCREMENT PRIMARY KEY,
    id_cliente INT,
    valor DECIMAL(10, 2) NOT NULL,
    metodo_pagamento ENUM('dinheiro', 'pix', 'cartão') NOT NULL,
    data_pagamento TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id_cliente) ON DELETE CASCADE
);
```

## 16.2. Comandos INSERT gerando dados fictícios

```SQL
-- Inserindo clientes
INSERT INTO Cliente (nome, cpf, telefone, email) VALUES
('Ana Silva', '12345678901', '11987654321', 'ana.silva@email.com'),
('Carlos Souza', '10987654321', '11876543210', 'carlos.souza@email.com'),
('Mariana Lima', '98765432100', '11765432109', 'mariana.lima@email.com');

-- Inserindo animais
INSERT INTO Animal (id_cliente, nome, tipo, descricao, condicao_medica, tipo_racao, habitos, rfid) VALUES
(1, 'Rex', 'cachorro', 'Cachorro de grande porte, muito ativo.', NULL, 'Ração A', 'Brincar, correr', 'RFID123456'),
(1, 'Miau', 'gato', 'Gato persa, muito calmo.', 'Alergia a poeira', 'Ração B', 'Dormir, brincar', 'RFID654321'),
(2, 'Bolinha', 'cachorro', 'Cachorrinho pequeno, adora companhia.', NULL, 'Ração A', 'Brincar, passear', 'RFID987654');

-- Inserindo veterinários
INSERT INTO Veterinario (nome, especializacao, plantao) VALUES
('Dr. Pedro Almeida', 'Clínico Geral', TRUE),
('Dra. Luiza Fernandes', 'Cirurgião', FALSE),
('Dr. Ricardo Costa', 'Dermatologia', TRUE);

-- Inserindo atendimentos
INSERT INTO Atendimento (id_cliente, id_animal, id_veterinario, data_hora, tipo_atendimento, formulario, prontuario, receita) VALUES
(1, 1, 1, '2024-09-20 10:00:00', 'rotina', 'Exame de rotina realizado.', 'Sem anormalidades.', 'Receita de ração e vermífugo.'),
(2, 3, 3, '2024-09-21 11:00:00', 'emergencia', 'Emergência - cachorro machucado.', 'Fraturas leves.', 'Receita de antibióticos.');

-- Inserindo hospedagens
INSERT INTO Hospedagem (id_cliente, id_animal, data_inicio, data_fim, cuidados) VALUES
(1, 1, '2024-09-25', '2024-09-30', 'Alimentação e passeios diários.');

-- Inserindo internações
INSERT INTO Internacao (id_cliente, id_animal, motivo, data_inicio, data_fim) VALUES
(2, 3, 'Cirurgia para remoção de tumor', '2024-09-22', '2024-09-24');

-- Inserindo creches
INSERT INTO Creche (id_animal, data, plano) VALUES
(1, '2024-09-26', 'Plano Mensal'),
(3, '2024-09-26', 'Plano Diário');

-- Inserindo produtos
INSERT INTO Produto (nome, categoria, preco, descricao) VALUES
('Ração A', 'Alimentação', 50.00, 'Ração premium para cães.'),
('Ração B', 'Alimentação', 45.00, 'Ração especial para gatos.'),
('Brinquedo para cães', 'Brinquedos', 20.00, 'Brinquedo resistente e durável.');

-- Inserindo pagamentos
INSERT INTO Pagamento (id_cliente, valor, metodo_pagamento) VALUES
(1, 100.00, 'cartão'),
(2, 200.00, 'dinheiro');
```
