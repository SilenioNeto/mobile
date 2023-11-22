# React Native Booklist Project 📚📖

<div align="center">
<img alt="App working" src="https://github.com/SilenioNeto/mobile/assets/88147887/d371f8b0-db77-4a3e-a328-6bb375c84622" width="250px">
</div>

## Overview
The React Native Booklist Project is a mobile application that allows users to create a personalized booklist, favorite books, and add comments. This project is built using React Native, a popular framework for building cross-platform mobile applications.

## Requirements
Before you can run the project, make sure you have the following installed on your machine:

* `Node.js`: Download and [install Node.js](https://nodejs.org/en/download/)
* `NPM` (Node Package Manager): Installed with Node.js
* `React Native CLI`: Install globally using the following command:
```bash
npm install -g react-native-cli
```
* [Expo](https://expo.dev/) mobile app: Tool used in mobile development with React Native that allows access to native APIs of the device withou installing dependencies or altering native code.

## Getting Started
Clone the repository to your local machine:

```bash
git clone https://github.com/SilenioNeto/mobile.git
```

* Install dependencies:

```bash
npm install
```

## Running the App on Android

1. Run the following command inside the app folder to start metro bundler
```bash
npm start
```

2. Download [expo](https://expo.dev/) app on your android phone
3. Then, you can scan the QR Code in your Android phone to see the app working 

## Features

1. Bookapp HomeScreen: Access screen to the books.
<div align="center">
<img alt="Home screen Print" src="https://github.com/neillane-carvalho/images/blob/main/VideoCapture_20231122-180417.jpg" width="250px">
</div>

3. Booklist Screen: View a list of books.
<div align="center">
<img alt="Book list Print" src="https://github.com/neillane-carvalho/images/blob/main/VideoCapture_20231122-180429.jpg" width="250px">
</div>

5. Favorite Books: Mark books as favorites.
<div align="center">
<img alt="Favorite Books Print" src="https://github.com/neillane-carvalho/images/blob/main/VideoCapture_20231122-180440.jpg" width="250px">
</div>

6. Comments: Add comments to books.
<div align="center">
<img alt="Comments Print" src="https://github.com/neillane-carvalho/images/blob/main/VideoCapture_20231122-180434.jpg" width="250px">
</div>

## Project Structure

```    
src/
|-- pages/
|   |-- Favoritos.js
|   |-- Home.js
|   |-- Livro.js
|   |-- Menu.js
|-- Routes.js
```

### `src/pages/Favoritos.js` 
    
    import React, { useState, useEffect } from 'react';
    
    import AsyncStorage from '@react-native-async-storage/async-storage';

    const response = await axios.get('https://api-livros.azurewebsites.net/livros');

      setFavoritos(favoriteList);
      
- Importações necessárias do React Native, incluindo `useState`, `useEffect`, e componentes como `View`, `Text`, `ScrollView`, `Button`.
- Utilização do AsyncStorage para armazenamento local de dados.
- Uso do axios para fazer solicitações HTTP.
- Componente Favoritos que renderiza uma lista de livros favoritos.
- Uso do useEffect para buscar dados de uma API e do useState para gerenciar os favoritos.
- Renderização dos livros favoritos em um ScrollView.
- Cada item da lista exibe detalhes do livro e um botão "Detalhes" que leva a informações adicionais sobre o livro.

### `src/pages/Home.js` 

- Imagem de Fundo Dinâmica: Utiliza `ImageBackground` para exibir uma imagem de fundo, trazendo uma experiência visual envolvente.
- Elementos de Texto: Apresenta um título, uma mensagem de boas-vindas e instruções para acessar os livros.
- Botões Navegacionais: Fornece botões interativos que levam os usuários para diferentes seções do aplicativo, como o menu principal e a lista de favoritos.
- Estilização Personalizada: Estilos cuidadosamente aplicados para garantir uma aparência agradável e consistente com o tema do aplicativo, usando cores, tipografia e layout.
  

### `src/pages/Livro.js` 

- O componente `Livro.js` é responsável por exibir os detalhes de um livro específico. Aqui estão os aspectos mais importantes:
- Carregamento de Dados Salvos: Utiliza `AsyncStorage` para carregar dados previamente salvos, como comentários e status de favorito para um livro.
- Edição de Comentários: Oferece um campo para adicionar comentários ou anotações sobre o livro.
- Marcação como Favorito: Fornece um botão de alternância (`Switch`) para marcar ou desmarcar o livro como favorito.
- Armazenamento Automático: Salva automaticamente os dados ao alterar os comentários ou a marcação como favorito.
- Botão Voltar: Permite ao usuário voltar para a tela anterior enquanto salva os dados atualizados.

### `src/pages/Menu.js` 
O componente `Menu`.js é responsável por exibir uma lista de livros disponíveis para os usuários. Aqui estão os principais aspectos:

- Consulta à API de Livros: Utiliza o `Axios` para buscar os dados dos livros de uma API externa.
- Lista de Livros: Apresenta os livros em um `ScrollView`, permitindo aos usuários rolar e visualizar os títulos disponíveis.
- Navegação para Detalhes do Livro: Ao tocar em um livro, direciona os usuários para a página de detalhes do livro (`Livro`), exibindo informações como nome, autor e tipo.
- Estilo e Interface Amigável: Oferece uma interface agradável com um título, lista de livros com detalhes visuais e uma opção para retornar à página inicial.

### `src/Routes.js`
O arquivo `Routes.js` é responsável por configurar a navegação entre as diferentes telas do aplicativo. Aqui estão os principais aspectos:

- Navigation Container: Utiliza o NavigationContainer fornecido pelo React Navigation para envolver a estrutura de navegação do aplicativo.
- Stack Navigator: Cria um StackNavigator para gerenciar as diferentes telas.
- Configuração de Telas: Define telas como `Home`, `Menu`, `Livro` e `Favoritos` vinculando-as aos componentes correspondentes. Além disso, controla a visibilidade do cabeçalho (header) para - - algumas telas, configurando `headerShown` para `false` ou `true`.
- Roteamento entre Telas: Permite a transição suave entre as telas do aplicativo de acordo com a navegação do usuário.

## Acknowledgments
Special thanks to [SilenioNeto](https://github.com/SilenioNeto), [silaspassos](https://github.com/silaspassos), [armentanoc](https://github.com/armentanoc) and [neillane-carvalho](neillane-carvalho) for their valuable contributions.
