# Desafio 1 - Base de dados do DETRAN

Este desafio tem como objetivo exercitar os conceitos de modelagem de dados e de banco de dados relacionais.

Caso surjam dúvidas, você pode utilizar o canal da capacitação no slack, contatar algum membro ou conversar com seu squad.

Você deve realizar um fork deste repositório para sua conta pessoal no GitHub. A entrega só será considerada válida se estiver incluída em uma release no GitHub. Se o candidato não souber como realizar um Fork, Commit, Push e uma Release no GitHub, deverá pesquisar ou pedir ajuda. O desafio também avaliará sua independência.

## Enunciado

O DETRAN deseja estabelecer um banco de dados para monitorar as infrações ocorridas no estado.

Os **veículos** são identificados pela **placa** e apresentam detalhes como **chassi**, **cor** predominante, **modelo**, **categoria** e **ano** de fabricação.

Cada veículo tem um **modelo**, como GOL MI, GOL 1.8, UNO CS, etc., sendo cada modelo identificado por um **número de 6 dígitos**.

A **categoria**, como AUTOMÓVEL, MOTOCICLETA, CAMINHÃO, entre outros, deve ser atribuída a cada veículo, com cada categoria identificada por um **número de 2 dígitos**.

Cada veículo tem um único **proprietário**, que é identificado pelo seu **CPF**. É necessário conhecer o **nome**, **endereço**, **bairro**, **cidade**, **estado**, **telefones**, **sexo**, **data de nascimento** e **idade** do proprietário.

Uma **infração** é descrita pelo **veículo infrator**, **data/hora** e **tipo de infração**.

Existem vários **tipos de infração**, como AVANÇO DE SINAL VERMELHO, PARADA SOBRE A FAIXA DE PEDESTRES, entre outros, sendo cada tipo identificado por um **número inteiro**. A cada tipo de infração está associado um **valor (preço)** que deve ser cobrado na ocorrência da infração. Também é importante registrar o **local** da infração, a **velocidade** aferida (se possível) e o **agente de trânsito** que registrou a infração.

Cada **local** é identificado por sua posição geográfica (**latitude e longitude** no globo terrestre). Além disso, é necessário armazenar a **velocidade permitida** no local, se possível.

Um **agente** de trânsito é identificado por sua **matrícula** funcional (um número inteiro) e também é descrito com o **nome**, **data de contratação** e **tempo de serviço** em meses completos.

## Desafio

A desafio consiste em entregar 5 arquivos:

- **DER** - diagrama entidade-relacionamento elaborado na ferramenta brModelo;
- **DLD** - diagrama lógico de dados elaborado na ferramenta brModelo;
- Script **Físico**: script sql para criação do banco de dados e suas tabelas;
- Script **Popula**: script sql para popular o banco de dados com dados fictícios, mas coerentes com o modelo de dados (mínimo de 5 registros por tabela);
- Script **Consulta**: script sql com as consultas (SELECT) solicitadas abaixo:
  - **A)** Apresentar todos os dados dos veículos de um determinado proprietário (informado pelo usuário através do CPF);
  - **B)** Consultar proprietário(s) por qualquer parte do nome;
  - **C)** Mostrar os dados da infração e do veículo que tiveram infrações cadastradas no Detran em um período (ou data) no padrão DE... ATÉ...;
  - **D)** Pesquisar o número de veículos que foram cadastrados em cada modelo, ordenando pelo número de veículos em ordem decrescente;

## Entrega

- A entrega do desafio deve ser realizada através de uma Release no GitHub.
  - Crie a release no seu repositório pessoal e envie o zip pelo google classroom.
- O candidato não deve excluir o repositório e nem a release após a entrega, pois a utilização do GitHub será avaliada.
