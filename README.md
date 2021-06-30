# GeoSapiens: Desafio técnico para Front End do Coletum

Este é um desafio que iremos utilizar para avaliar os conhecimentos técnicos do(a)s candidato(a)s interessado(a)s na vaga de Front End disponível na GeoSapiens.

# Contextualização

O Coletum é um sistema propriétario da GeoSapiens (https://coletum.com) oferecido em formato SaaS. Ele é uma plataforma para coleta e gestão de dados voltada principalmente a empresas que frequentemente coletam dados em ambientes fora do escritório ou em campo.

O processo de uso do Coletum se inicia no sistema web, onde os usuários configuram a estrutura dos formulários através de uma interface web (de forma bastante similar ao Google Forms). Após os formulários serem construídos / estruturados, os usuários podem preenchê-los através de uma interface web ou de um aplicativo para dispositivo móvel.

O Coletum dispõe de um webservice (graphql) para consumo dos preenchimentos, dos formulários e das estrutura dos formulários.

Documentação do webservice: https://coletum.docs.apiary.io

# O Desafio

O desafio consiste na criação de duas interfaces web utilizando React para ações distintas do usuário envolvendo o webservice do Coletum. 

1. Uma tela de cadastro de um formulário específico; e

1. Uma tela de apresentação dos preenchimentos existentes para um formulário específico.

## Instruções

1. Crie um `fork` deste projeto para desenvolver o seu desafio.

1. Use o `README` principal do respositório para nos contar um pouco sobre como foi desenvolver a solução do desafio, decisões tomadas e principalmente as instruções de como rodar o seu projeto. Essa parte é muito importante, já quem quem irá rodar o seu projeto não é uma pessoa especialista em frontend, e se conseguir explicar pra ela as etapas do processo é um bom começo.

1. Ao finalizar o desafio, envie um e-mail para <vemprageo@geosapiens.com.br> com o título do e-mail `Desafio Coletum front-end - seu nome`, e contendo o link para o seu `fork` no corpo do e-mail.

1. Esse é um desafio técnico e não existe apenas uma resposta correta. Mostre a sua técnica de solução de problemas e criatividade, independente do seu nível de experiência, mas não esqueça do objetivo do desafio.

## Desafio #1 Tela de cadastro de preenchimento

Acessar a estrutura do formulário indicado através do __webservice__ do Coletum, e com base na estrutura apresentada, criar uma interface web em React para a criação de preenchimentos deste formulário.

Lembrando que a tela deve ter um botão de ação `mockup` para enviar o formulário preenchido que apresente a forma de envio dos dados.

O formulário já foi criado no Coletum e é chamado "Filmes Preferidos", sendo um cadastro simples dos seus filmes preferidos.

A estrutura do formulário está disponível na URL:
<https://coletum.com/api/graphql?query={form_structure(formId:23458){label,componentId,type,helpBlock,order,options,minimum,maximum,widget,components{label,componentId,type,options,minimum,maximum,widget,components{label,componentId,type,options,minimum,maximum,widget,components{label,componentId,type,options,minimum,maximum,widget,components{label,type,options,minimum,maximum,widget}}}}}}&token=7s5txcu909kwc48wookgw8g00occokk>

Este formulário possui os seguintes campos:
- Nome do filme: campo textual;
- Categorias: campo de múltipla escolha;
- Avaliação pessoal: campo “estrela” (0 a 5 estrelas);
- Data de lançamento: campo de data; e
- URL para o site do IMDB com informações sobre o filme: campo URL.

Lembre-se de criar uma interface para preenchimento ***dinâmica***, ou seja, ela deve se adaptar a estrutura do formulário recebida pelo webservice e não ser fixa com as questões deste formulário de teste. Não se preocupe com outros tipos de campos, contemple apenas “textual”, “seleção múltipla”, “data”, “estrela” e “URL”.

## Desafio #2 Tela de listagem de preenchimentos

Acessar a listagem de preenchimentos existentes para o formulário "Filmes Preferidos", através da rota do __webservice__, e criar uma interface web em React para a apresentação da listagem dos preenchimentos existentes e um botão de ação para a visualização completa do preenchimento em questão.

A listagem de preenchimentos do formulário está disponível na URL:
<https://coletum.com/api/graphql?query={answer(formId:23458){answer{nomeDoFilme302645,categorias302641,avaliacaoPessoal302642,dataDeLancamento302643,urlParaOSiteDoDoImdbComInformacoesSobreOFilme302644},metaData{userId,userName,createdAtSource,friendlyId,createdAt,createdAtDevice,createdAtCoordinates,updatedAt,updatedAtCoordinates}}}&token=7s5txcu909kwc48wookgw8g00occokk>

## O que avaliaremos no seu desafio

1. Contexto geral do resultado final de acordo com o nível de experiência;

1. Histórico de commits do git;

1. As instruções para rodar o projeto;

1. Organização, semântica, estrutura, legibilidade, manutenibilidade do seu código;

1. A implementação da forma de consumo dos dados através do webservice do Coletum;

1. O controle do estado da aplicação (com redux ou mobx);

1. Alcance dos objetivos;

1. Componentização dos componentes; e

1. Responsividade do layout.

## Diferenciais opcionais do desafio

1. Testes unitários; e

1. Dockerização da aplicação.

