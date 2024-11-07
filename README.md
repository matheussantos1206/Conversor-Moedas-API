# Conversor-Moeda-Via API 💹

>## ``Introdução📰``

Este projeto é um conversor de moedas utilizando a API Exchangerate-API para buscar as taxas de câmbio em tempo real entre diferentes moedas. O objetivo é fornecer uma interface simples onde o usuário pode informar um valor em uma moeda e convertê-lo para outra moeda de sua escolha.

>## ``Funcionalidades🔨``

- Conversão de valores entre duas moedas diferentes.
- Busca das taxas de câmbio em tempo real via API externa.
- Exibição do resultado de conversão diretamente na interface.
- Interface web simples e de fácil utilização.

>## ``Tecnologias💾``

- HTML5: Estrutura da página.
- CSS3: Estilização da página (não incluído no código fornecido, mas pode ser adicionado conforme necessário).
- JavaScript (ES6+): Lógica de conversão de moedas e interação com a API.
- API Exchangerate-API: Utilizada para obter taxas de câmbio em tempo real.

>## ``Como funciona📒``
- O usuário entra com um valor, a moeda de origem e a moeda de destino.
- O script faz uma chamada à API da Exchangerate-API para buscar a taxa de câmbio entre as duas moedas selecionadas.
- O valor informado pelo usuário é multiplicado pela taxa de câmbio e o resultado é mostrado na página.

## ``Estrutura do Projeto`` 

![estrutura projeto](/img/estrutura%20do%20c%C3%B3digo%20API.png)

O projeto consiste em um único arquivo JavaScript que se comunica com uma API externa para obter as taxas de câmbio. O fluxo de dados ocorre de forma assíncrona utilizando fetch e async/await.


* ### ``Arquivos``

* HTML: Não fornecido no código. Espera-se que exista um formulário HTML com os seguintes campos:
- input#valor: Campo de entrada para o valor a ser convertido.
- select#moeda1: Lista suspensa para selecionar a moeda de origem.
- select#moeda2: Lista suspensa para selecionar a moeda de destino.
- div#conversao: Onde o valor convertido será exibido.

* ### ``JavaScript``
![estrutura do js](/img/estrutura%20do%20js.png)
- apiKey: A chave da API para acessar os dados de conversão (não é recomendada a exposição de chaves em código público).
- getExchangeRate: Função assíncrona que realiza a consulta à API externa e retorna a taxa de câmbio.
- Escutador de eventos (submit) no formulário, que coleta os dados, chama a função getExchangeRate e exibe o resultado.

* ### ``Fluxo do Código``
- O usuário preenche o formulário com um valor e as duas moedas desejadas.
- Quando o formulário é enviado, o evento de submit é capturado e a função getExchangeRate é chamada para buscar a taxa de câmbio entre as moedas selecionadas.
- A função getExchangeRate utiliza a API do ExchangeRate-API para buscar as taxas de câmbio em tempo real.
- O valor informado pelo usuário é multiplicado pela taxa de câmbio para calcular o valor convertido.
- O valor convertido é exibido na tela na área designada.

## ``Funcionalidade da API``
O código utiliza a API do ExchangeRate-API para obter a taxa de câmbio entre as moedas. A URL de acesso à API é:

- ${apiKey} é a chave da API fornecida.
- ${moeda1} é a moeda de origem selecionada pelo usuário.

A API retorna as taxas de conversão entre a moeda de origem e várias outras moedas, incluindo a moeda de destino.


## ``Como Usar``
- Abra o arquivo HTML do projeto em seu navegador.
- Preencha o valor a ser convertido no campo "Valor".
- Selecione a moeda de origem (moeda1) e a moeda de destino (moeda2) nos menus suspensos.
- Clique no botão de enviar ou pressione Enter para calcular a conversão.
- O valor convertido será exibido abaixo do formulário.

## ``Erros Comuns``

- Erro ao buscar taxa de câmbio: Caso a API não consiga fornecer as taxas de câmbio, a mensagem de erro será exibida: "Erro ao buscar a cotação. Tente novamente".

- API Key inválida ou expirada: Verifique se a chave de API (apiKey) está correta e válida. Chaves expiram após um período.

- Problemas de rede: Se a API estiver inacessível ou a conexão de internet falhar, o erro será capturado e a mensagem "Error: ..." será exibida no console.

## ``Conclusão``

Este é um projeto simples e útil para conversão de moedas utilizando taxas de câmbio ao vivo. Ele pode ser expandido ou integrado em sistemas mais complexos, como aplicações financeiras ou plataformas de comércio eletrônico, para fornecer informações de câmbio precisas aos usuários.