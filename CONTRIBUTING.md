# Contribuindo com o site

Seguem instruções para contribuir com o site.

## Instalando

1. Instale [Ruby](https://www.ruby-lang.org/) no seu computador

2. Fork o repositório
   
3. Crie uma branch para a sua feature que você trabalhará
`git checkout -b <titulo-da-nova-branch>`

4. Instale a gem Jekyll
`gem install jekyll`

4. Rode o servidor local
`jekyll serve --watch`

5. Realize as modificações necessárias
   
6. Teste as modificações no seu ambiente local

7. Envie um pull request para o nosso repositório

----
## Modificando o Header

No header estão as informações gerais sobre o evento e o botão de inscrições, caso estejam abertas.
Altere o arquivo "_data/conference _[ano]/header.yml" seguindo as orientações abaixo:

```
- date: <data do evento>
  location: <endereço, se for um evento presencial>
  youtube-link: <preencha caso a conferencia seja remota ou se for transmitida>
  inscription-link: <coloque o link apenas no período em que as inscrições estão abertas>
```

## Modificando o About

Essa é a sessão que fica logo abaixo da imagem principal da página, nela é descrito um breve resumo sobre o "Women in Data Science Recife", considerando as exigências mínimas indicadas no Guia de Uso da Marca.

Altere o arquivo "_includes/conference _[ano]/about.html"

## Modificando o Facts

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

## Modificando o Schedule

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
   

## Adicionando Novo evento

Essa sessão é dedicada aos eventos secundários realizados ao longo do ano, seja na modalidade presencial ou remota.
No começo do arquivo "_data/other_events.yml", crie um novo bloco de conteúdo e adicione as informações conforme indicado abaixo:

```
- title: <título do evento>
  date: <data>
  time: <horário>
  location: <local e endereço>
  resume: <resumo>
  image: /assets/images/events/<titulo-arquivo.png>
  describe_image: <descrição da imagem para que ela esteja acessível a pessoas com deficiência visual> 
  link: <link com mais detalhes do evento>
```