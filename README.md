Projeto de Landing Page de Viagens com Vídeo de Fundo
Este projeto é uma landing page moderna e minimalista voltada para o tema de viagens, com um design imersivo que utiliza um vídeo de fundo para criar uma experiência visual envolvente. Vou explicar como funciona e como foi construído:
Visão Geral
Imagine uma página web que te transporta instantaneamente para uma experiência de viagem. Ao abrir a página, você é recebido por um vídeo em tela cheia mostrando paisagens incríveis, com um título grande e impactante "Travel" no centro da tela, acompanhado por um botão "Explore" logo abaixo. É uma página simples, mas muito eficaz para capturar a atenção do visitante.
Estrutura HTML
O HTML forma a base da nossa página. É relativamente simples:
htmlCopy<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Travel Page</title>
    <!-- Aqui viria o link para o CSS externo -->
</head>
<body>
    <div class="hero">
        <video autoplay loop muted playsinline class="back-video">
            <source src="assets/video.mp4" type="video/mp4">
        </video>

        <div class="content">
            <h1>Travel</h1>
            <a href="#">Explore</a>
        </div>
    </div>
</body>
</html>
Temos um contêiner principal chamado "hero" que ocupa toda a tela. Dentro dele, temos dois elementos principais:

Um vídeo de fundo que roda automaticamente, em loop e sem som
Uma div "content" que contém o título "Travel" e o botão "Explore"

Estilização CSS
É no CSS que a mágica acontece. Vamos ver como cada parte contribui para o visual final:
cssCopy@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}
Aqui, começamos importando a fonte Poppins do Google Fonts, que dá um visual moderno e clean à página. O seletor universal (*) remove margens e preenchimentos padrão do navegador e aplica a fonte Poppins a todos os elementos.
cssCopy.hero {
    width: 100%;
    height: 100vh;
    background-image: linear-gradient(rgba(12,3,51,0.3), rgba(12,3,51,0.3));
    position: relative;
    padding: 0 5%;
    display: flex;
    justify-content: center;
    align-items: center;
}
O contêiner hero é configurado para ocupar 100% da largura e altura da tela (100vh). Usamos um gradiente linear semi-transparente sobre toda a tela, que dá um tom escuro e dramático ao fundo, ajudando a melhorar a visibilidade do texto. O display flex com justify-content e align-items configurados para center garante que todo o conteúdo fique perfeitamente centralizado.
cssCopy.back-video {
    position: absolute;
    right: 0;
    bottom: 0;
    z-index: -1;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
O vídeo de fundo tem posição absoluta e z-index negativo para ficar atrás de todo o conteúdo. O object-fit: cover garante que o vídeo cubra toda a área da tela sem distorções, independentemente do tamanho da janela.
cssCopy.content {
    text-align: center;
    color: white;
}

.content h1 {
    font-size: 160px;
    font-weight: 600;
    margin-bottom: 20px;
}

.content a {
    text-decoration: none;
    display: inline-block;
    color: #fff;
    font-size: 24px;
    border: 2px solid white;
    padding: 14px 70px;
    border-radius: 50px;
    margin-top: 20px;
    transition: 0.3s ease;
}

.content a:hover {
    background-color: white;
    color: rgba(12,3,51,1);
}
Aqui estilizamos o conteúdo central. O texto é branco para contrastar com o fundo escuro. O título "Travel" é enorme (160px) e impactante. O botão "Explore" tem uma borda branca e se transforma quando o mouse passa por cima, mudando para fundo branco e texto escuro, criando um efeito de interação agradável.
O que torna este projeto especial?

Simplicidade eficaz: Com apenas dois elementos principais (título e botão), a página consegue transmitir seu propósito de forma clara e direta.
Experiência imersiva: O vídeo de fundo cria uma sensação de movimento e imersão que uma imagem estática não conseguiria.
Design responsivo: A estrutura flexível se adapta a diferentes tamanhos de tela, mantendo a experiência visual em qualquer dispositivo.
Interatividade sutil: O efeito hover no botão adiciona uma camada de interatividade sem ser excessivo.
Performance: O vídeo roda em loop, sem som e automaticamente, sem interferir na experiência do usuário.

Esta landing page é um excelente exemplo de como elementos simples, quando bem combinados, podem criar uma experiência web memorável e eficaz para atrair visitantes interessados em viagens
