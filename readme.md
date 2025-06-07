# Fundamentos de React - Formação Rocketseat 🚀

![Capa do Projeto](https://social-share-image.vercel.app/image?file=rocketseat-react-fundamentos&template=default&title=Fundamentos%20do%20React.js&description=Reposit%C3%B3rio%20com%20os%20conceitos%20iniciais%20de%20React,%20abordando%20componentiza%C3%A7%C3%A3o,%20Babel,%20estiliza%C3%A7%C3%A3o%20e%20o%20uso%20da%20CDN.&author=SEU_NOME_AQUI&avatar=https://github.com/SEU_USUARIO_AQUI.png)

## 📝 Sobre o Projeto

Este repositório documenta minha jornada de aprendizado nos fundamentos do **React.js**, como parte da formação oferecida pela [Rocketseat](https://www.rocketseat.com.br/). O objetivo principal foi compreender os pilares essenciais do React, desde sua definição e propósito até a criação de componentes funcionais e estilizados.

O projeto consiste em uma página simples, construída sem o uso de um ambiente de desenvolvimento complexo (como o `create-react-app`), utilizando diretamente o **React via CDN**. Isso permitiu um foco total nos conceitos básicos, como a transpilação em tempo real pelo **Babel** e a renderização de componentes no DOM.

---

## 🧠 Conceitos Abordados

Durante este módulo de fundamentos, os seguintes tópicos foram explorados e aplicados:

-   **O que é React?**: Entendimento do React como uma biblioteca para criar interfaces de usuário e não um framework completo.
-   **Componentização**: A prática de dividir a UI em partes independentes e reutilizáveis, a base do desenvolvimento com React.
-   **React via CDN vs. Bundler**: As diferenças entre usar o React diretamente no navegador e utilizar ferramentas de build como Vite ou Webpack.
-   **Transpilação com Babel**: A importância do Babel para converter o código JSX e funcionalidades modernas do JavaScript em uma sintaxe que os navegadores entendem.
-   **Estilização no React**:
    -   CSS Inline
    -   CSS Modules
    -   CSS-in-JS (Styled Components)
    -   Pré-processadores como SASS
    -   Frameworks de CSS (TailwindCSS)

---

## 🛠️ Tecnologias Utilizadas

Este projeto foi construído utilizando as seguintes ferramentas, todas linkadas via CDN:

-   **React**: A biblioteca para a construção da interface.
-   **React DOM**: O pacote responsável por renderizar os componentes React no navegador.
-   **Babel (Standalone)**: Para transpilar o JSX em tempo real, diretamente no browser.
-   **TailwindCSS (via CDN)**: Para estilização rápida e moderna, baseada em classes de utilitário.

---

## 💻 O Código

Abaixo está o código-fonte desenvolvido, que demonstra a criação de um componente de botão reutilizável (`Button`) e sua utilização dentro de um componente principal (`App`).

```html
<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rocketseat - React.js - Fundamentos</title>
</head>

<body>
    <div id="root"></div>
    
    <script src="[https://unpkg.com/@tailwindcss/browser@4](https://unpkg.com/@tailwindcss/browser@4)"></script>
    <script crossorigin src="[https://unpkg.com/react@18/umd/react.development.js](https://unpkg.com/react@18/umd/react.development.js)"></script>
    <script crossorigin src="[https://unpkg.com/react-dom@18/umd/react-dom.development.js](https://unpkg.com/react-dom@18/umd/react-dom.development.js)"></script>
    <script crossorigin src="[https://unpkg.com/@babel/standalone/babel.min.js](https://unpkg.com/@babel/standalone/babel.min.js)"></script>

    <script type="text/babel">

        // Objeto para mapear as variantes de cor do botão
        const VariantButtonColor = {
            default: 'bg-gray-500 hover:bg-gray-600',
            success: 'bg-green-500 hover:bg-green-600',
        }

        // Componente de Botão reutilizável
        function Button({ children, variant = 'default', className, ...props }){
            return(
                <button 
                    className={`
                        px-5 py-2 rounded text-white font-bold transition-colors
                        ${VariantButtonColor[variant]}
                        ${className}
                    `} 
                    {...props}
                > 
                    { children } 
                </button>
            )
        }

        // Componente Principal da Aplicação
        function App(){
            return(
                <main className="flex gap-4 p-4 bg-gray-900 min-h-screen items-start">
                    <Button 
                        variant="success" 
                        title="Botão com variante de sucesso"
                    >
                        Botão Sucesso
                    </Button>
                    
                    <Button title="Botão com variante padrão">
                        Botão Padrão
                    </Button>
                </main>
            )
        }

        // Renderiza a aplicação na div #root
        const rootElement = document.getElementById('root');
        const root = ReactDOM.createRoot(rootElement);
        root.render(<App />);

    </script>

</body>
</html>

---

## ✨ Resultado Visual



---

## 🚀 Como Executar

Por ser um projeto autocontido que utiliza CDNs, não há necessidade de instalação de dependências ou de um servidor de desenvolvimento.

Basta clonar o repositório e abrir o arquivo index.html diretamente em seu navegador de preferência.

```bash
# Clone este repositório
$ git clone [https://github.com/SEU_USUARIO_AQUI/NOME_DO_REPOSITORIO.git](https://github.com/SEU_USUARIO_AQUI/NOME_DO_REPOSITORIO.git)

# Acesse o diretório
$ cd NOME_DO_REPOSITORIO

# Abra o arquivo index.html no navegador

<hr>

Feito com ❤️ por Felipe Manoel Silva. Agradecimentos especiais à Rocketseat pelo conteúdo incrível!