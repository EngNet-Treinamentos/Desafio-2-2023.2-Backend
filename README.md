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

## Entrega

DER - diagrama entidade-relacionamento elaborado na ferramenta brModelo na
versão 3.31 ou superior;
DLD - diagrama lógico de dados elaborado na ferramenta brModelo na versão 3.31
ou superior;
Script Fisico: script somente de criação com as restrições fundamentais das
tabelas, respeitando as lógicas de criação no banco de dados e criando a base de
dados somente se ela não existir, conforme estudado em aulas anteriores e usando
uma única instrução procedural coerente no MySQL;
Script Popula: script que somente insere dados no banco de dados,
respeitando suas regras e lógicas modeladas com mínimo de 5 tuplas por tabela;
Script Consulta: As consultas deverão estar em outro script (Consultas) que você
deverá elaborar para concluir esta atividade da disciplina.
Uma instrução SELECT deverá ser elaborada para cada uma das demandas
apresentadas a seguir e que estarão no outro
novo script bem documentado (com cabeçalho coerente). Reflitam sobre a
apresentação dos dados resultantes de cada
pesquisa que deveriam ser apresentados de maneira satisfatória para os seus
usuários finais.
A) Apresentar todos os dados dos veículos de um determinado proprietário
fornecido pelo usuário, relacionando por extenso a
categoria que cada um é classificado (implementar tal consulta através de uma
VIEW que respeite as propriedades
esclarecidas ao final desta lista de consultas) ;
B) Consultar proprietário(s) por qualquer parte do nome fornecido pelo usuário;
C) Mostrar os dados da infração e do veículo que tiveram infrações cadastradas no
Detran em um período (ou data) no
padrão DE... ATÉ...;
D) Pesquisar quantos veículos existem cadastrados por Modelo, inclusive
apresentando os modelos cadastrados que não
tiverem nenhum veículo cadastrado, se existir tal situação

- A entrega do desafio deve ser realizada através de uma Release no GitHub.
  - Crie a release no seu repositório pessoal e envie o zip pelo google classroom.
- O candidato não deve excluir o repositório e nem a release após a entrega, pois a utilização do GitHub será avaliada.
