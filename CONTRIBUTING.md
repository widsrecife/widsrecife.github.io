# Contribuindo com o site

Seguem instruções para contribuir com o site.

## Instalando

1. Instale [Ruby](https://www.ruby-lang.org/) no seu computador

2. Fork o repositório
   
3. Crie uma branch para a sua feature que você trabalhará
```
git checkout -b <titulo-da-nova-branch>
```

4. Instale a gem Jekyll
```
gem install jekyll
```

4. Rode o servidor local
```
jekyll serve --watch
```

5. Realize as modificações necessárias
   
6. Teste as modificações no seu ambiente local

7. Envie um pull request para o nosso repositório

----
## SUMÁRIO
[Modificando o Menu](#navbar)
[Modificando o Header](#header)
[Modificando o Sobre](#about)
[Modificando a Visualização resumida dos dados do evento](#facts)
[Modificando a Programação](#schedule)
[Adicionando nova mulher em Facilitadoras](#speakers)
[Adicionando nova empresa em Apoiadoras](#partners)
[Modificando a FAQs](#faq)
[Adicionando novo evento em Outros Eventos](#otherevents)
[Atualizando os links do Rodapé](#footer)


## Modificando o Menu <div id='navbar' />

Essa sessão é dedicada a navegação da página.

Altere o arquivo "_includes/navbar.html"


## Modificando o Header <div id='header' />

No header estão as informações gerais sobre o evento e o botão de inscrições, caso estejam abertas.

Altere o arquivo "_data/conference _[ano]/header.yml" seguindo as orientações abaixo:

```
- date: <data do evento>
  location: <endereço, se for um evento presencial>
  youtube-link: <preencha caso a conferencia seja remota ou se for transmitida>
  inscription-link: <coloque o link apenas no período em que as inscrições estão abertas>
```

Sugerimos que a imagem de background do Header seja referente a última conferência. Para modificá-la, altere a classe "site-header" do arquivo "assets/css/conference_[ano].css".


## Modificando o Sobre <div id='about' />

Essa sessão é uma breve descrição sobre o "Women in Data Science Recife", considerando as exigências mínimas indicadas no Guia de Uso da Marca.

Altere o arquivo "_includes/conference _[ano]/about.html"


## Modificando a Visualização resumida dos dados do evento <div id='facts' />

Visualização resumida dos dados do evento.

Altere o arquivo "_data/conference _[ano]/facts.yml" seguindo as orientações abaixo:

```
- day: <dia> <mês abreviado>
  year: "<ano>"
  hour: "<horário de início>"
  location: <nome do local>
  location-link: <se presencial, link do Google Maps. Se remoto, link da plataforma de stream>
  inscription-status: <status das inscrições: em breve, abertas, encerradas>
  inscription-link: <link para inscrições>
```


## Modificando a Programação <div id='schedule' />

Sessão dedicada a exibição da programação completa do evento.

1. Altere as datas de cada tabela no arquivo "_includes/conference _[ano]/schedule.html".

2. Em seguida, modifique o arquivo "_data/conference _[ano]/schedule.yml" seguindo as orientações abaixo:

```
- day: <dia de evento que a palestra ocorrerá, ex: 1, 2>
  hour: "<horário de início>"
  title: <título da palestra>
  speaker: <nome da palestrante>
```

3. Caso o evento não seja de 2 dias, sugerimos modificar o tipo da "div" subordinada a "div class=row" no arquivo "_includes/conference _[ano]/schedule.html".


## Adicionando nova mulher em Facilitadoras <div id='speakers' />

Nessa sessão devem estar todas as mulheres que participam da programação, seja palestrante, mediadora, facilitadora de oficina.

1. Todas as fotos devem ter a mesma proporção. Proporção sugerida: 1:1

2. Coloque a foto da facilitadora na pasta "assets/images/conference-[ano]/speakers"
   
3. No começo do arquivo "_data/conference _[ano]/speakers.yml", crie um novo bloco de conteúdo e adicione as informações conforme indicado abaixo:

```
- name: <nome>
  image: <titulo-arquivo.png>
  image_description: <descrição da imagem para que ela esteja acessível a pessoas com deficiência visual> 
  linkedin: <usuário linkedin>
  twitter: <usuária twitter>
  instagram: <usuária instagram> 
  site: <link para site>
```


## Adicionando nova empresa em Apoiadoras <div id='partners' />

Nessa sessão estarão todas as empresas patrocinadoras e apoiadoras do evento. Sugerimos ordená-las por grau de importância/contribuição dada ao evento, sendo a primeira responsável pelo maior aporte.

1. Coloque a logomarca da empresa na pasta "assets/images/conference-[ano]/partners"

2. Modifique o arquivo "_data/conference _[ano]/partners.yml" seguindo as orientações abaixo:

```
- name: <título da empresa>
  image: <titulo-arquivo.png>
  link: <link para site ou rede social da empresa>
```


## Modificando a FAQs <div id='faq' />

Nessa sessão estão todas as dúvidas recorrentes das participantes, com objetivo de ajudar as demais.

Modifique o arquivo "_data/faq.yml" seguindo as orientações abaixo:

```
- id: "<id único da pergunta>"
  question: <pergunta>
  answer: <resposta>
```


## Adicionando novo evento em Outros Eventos <div id='otherevents' />

Essa sessão é dedicada aos eventos secundários realizados ao longo do ano, seja na modalidade presencial ou remota.

1. Coloque o cartaz do evento na pasta "assets/images/conference-[ano]/events"

2. No começo do arquivo "_data/other_events.yml", crie um novo bloco de conteúdo e adicione as informações conforme indicado abaixo:

```
- title: <título do evento>
  date: <data>
  time: <horário>
  location: <local e endereço>
  resume: <resumo>
  image: <titulo-arquivo.png>
  image_description: <descrição da imagem para que ela esteja acessível a pessoas com deficiência visual> 
  link: <link com mais detalhes do evento>
```


## Atualizando os links do Rodapé <div id='footer' />

Sessão dedicada aos canais de comunicação e redes sociais do grupo WiDS Recife, além disso apresenta a licença do site.

Modifique o arquivo "_data/footer.yml" seguindo as orientações abaixo:

```
- instagram: <usuária instagram>
  twitter: <usuária twitter>
  linkedin: <usuária linkedin>
  github: <usuária github>
  email: <e-mail de contato>
```