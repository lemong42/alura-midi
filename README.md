<h1 align="center">Alura MIDI</h1>

![GitHub Org's stars](https://img.shields.io/github/stars/lemong42/alura-midi?style=social)

![Banner do projeto Alura MIDI](https://user-images.githubusercontent.com/90742197/187320393-750419c2-4d16-41c7-850d-c25a519ae62c.png)

<img alt="Shield de status em desenvolvimento" src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=green&style=for-the-badge">
<img alt="Shield de last update no dia 29.08.2022" src="http://img.shields.io/static/v1?label=LAST%20UPDATE&message=29.08.2022&color=blue&style=for-the-badge">

Esse projeto foi desenvolvido para mergulhar na integração entre JavaScript com páginas web desenvolvidas com HTML e CSS. Nele criamos um MIDI no qual ao apertar uma tecla, seja com o mouse ou com o teclado, um som correspondente a tecla será reproduzido.

## Funcionalidades do projeto

`Funcionalidade 1`: tecla ativada diferenciada.

![Imagem da tecla ativa de cor diferente](https://user-images.githubusercontent.com/90742197/187320900-fb1abea1-cab8-4fc6-8218-95680fd1bbf6.png)

`Funcionalidade 2`: última tecla ativada diferenciada.

![Imagem da útima tecla ativada de cor diferente](https://user-images.githubusercontent.com/90742197/187320999-6ead02e1-6bbc-4d57-95dc-dd54ae8f8204.png)

`Funcionalidade 3`: reprodução de som ao pressionar uma tecla.

```js
function tocaSom (seletorAudio) {
    const elemento = document.querySelector(seletorAudio)
    
    if (elemento && elemento.localName === 'audio') {
        elemento.play();
    } else {
        console.log('Elemento não encontrado ou seletor inválido');
    }
}

for (i = 0; i < listaTeclas.length; i++) {
    const tecla = listaTeclas[i];
    const instrumento = tecla.classList[1];

    const idAudio = `#som_${instrumento}`;

    tecla.onclick = function () {
        tocaSom(idAudio);
    }
```

### Tecnologias utilizadas 

<div>
  <img align="center" alt="logo-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="logo-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="logo-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
</div>
