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
## Modificando o header

No header estão as informações gerais sobre o evento e o botão de inscrições, caso estejam abertas.
Altere o arquivo "_data/conference _[ano]/header.yml" seguindo as orientações abaixo:

```
- date: <data do evento>
  location: <endereço, se for um evento presencial>
  youtube-link: <preencha caso a conferencia seja remota ou se for transmitida>
  inscription-link: <coloque o link apenas no período em que as inscrições estão abertas>
```

## Adicionando um novo evento

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