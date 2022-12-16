# Desafio Loopstudios Landing Page - Frontend-Mentor

Este é um desafio de uma landing page para a empresa Loopstudios proposto pelo site Frontend-Mentor.

## Tabela de Conteúdos

- [Visão Geral](#visão-geral)
    - [Imagens](#imagens)
    - [Link da página](#link)
- [Processo](#processo)
    - [Linguagens utilizadas](#linguagens-utilizadas)
    - [O que aprendi](#o-que-aprendi)
    - [Possíveis evoluções](#possíveis-evoluções)
- [Autor](#autor)

## Visão-geral

### Imagens

<br>

````
Versão de Desktop
````

   <img src="./src/design/desktop-design.gif" alt="desktop-design">

<br>

````
Versão Mobile
````

 <img src="./src/design/mobile-design.gif" alt="mobile-design">

### Link

- Página no GitHub Pages: <a href="https://julio-mansan2.github.io/loopstudios-landing-page">Clique aqui!</a>

## Processo

### Linguagens utilizadas

<br>

- Marcações semânticas de HTML5
- Propriedades de customização do CSS3
- Estruturas de JavaScript

<br>

### O que aprendi

<br>

- Criar um menu hambúrguer:

````html

<input id="menu__toggle" type="checkbox" />
<label class="menu__btn" for="menu__toggle">
<span></span>
</label>

````

````css

    #menu__toggle {
        opacity: 0;
    }

    #menu__toggle:checked+.menu__btn>span {
        transform: rotate(45deg);
    }

    #menu__toggle:checked+.menu__btn>span::before {
        top: 0;
        transform: rotate(0deg);
    }

    #menu__toggle:checked+.menu__btn>span::after {
        top: 0;
        transform: rotate(90deg);
    }

    .menu__btn {
        top: 40px;
        right: 7%;
        position: absolute;
        width: 26px;
        height: 26px;
        cursor: pointer;
        z-index: 1;
    }

    .menu__btn>span,
    .menu__btn>span::before,
    .menu__btn>span::after {
        display: block;
        position: absolute;
        width: 100%;
        height: 2px;
        background-color: hsl(0, 0%, 100%);
        transition-duration: .25s;
    }

    .menu__btn>span::before {
        content: '';
        top: -8px;
    }

    .menu__btn>span::after {
        content: '';
        top: 8px;
    }

    .header ul {
        position: absolute;
        top: 0;
        width: 100%;
        gap: 20px;
        height: 100%;
        left: -100%;
        padding: 7%;
        flex-direction: column;
        justify-content: center;
        background-color: #000;
        background-size: contain;
        transition-duration: .25s;
    }

````

- Aplicar uma função ao menu hambúrguer:

````html

<input id="menu__toggle" type="checkbox" />
<label class="menu__btn" for="menu__toggle">
<span></span>
</label>

````
````javascript

const menuHamburguer = document.getElementById('menu__toggle')
const navMenu = document.getElementById('menu_box')

menuHamburguer.addEventListener('click', function () {
    if (menuHamburguer.checked) {
        navMenu.classList.add('aparecer')
    } else {
        navMenu.classList.remove('aparecer')
        navMenu.classList.add('ocultar')
    }
})

````
<br>

### Possíveis evoluções

<br>

- Códigos mais compactos;
- Abdicar das definições manuais de medição para container;
- Aplicar o efeito correto de :hover.

<br>

## Autor

GitHub - <a href="https://github.com/julio-mansan2">julio-mansan2</a> <br>
Front-end Mentor - <a href="https://www.frontendmentor.io/profile/julio-mansan2">julio-mansan2</a> <br>