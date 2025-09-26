// -------------------------------
// SELEÇÃO DE ELEMENTOS DO HTML
// -------------------------------

// Botão de conversão
const buttonConvert = document.querySelector(".button-convert");

// Input de valor a converter
const inputConvert = document.querySelector(".input-convert");

// Selects de moedas
const selectConvertOne = document.querySelector(".select-convert-one");
const selectConvertTwo = document.querySelector(".select-convert-two");

// Boxes das moedas
const currencyBoxOne  = document.querySelector(".currency-box-one");
const currencyBoxTwo = document.querySelector(".currency-box-two");

// Nomes e valores exibidos
const currencyOne = document.querySelector(".currency-one");
const currencyTwo = document.querySelector(".currency-two");
const currencyValueOne = document.querySelector(".currency-value-one");
const currencyValueTwo = document.querySelector(".currency-value-two");

// -------------------------------
// FUNÇÕES DE BACKGROUND E HINOS
// -------------------------------

// Troca o fundo de acordo com a moeda de destino
function trocarBackground(moeda) {
    const fundos = {
        real: "./img/brasil.jpg",
        dolar: "./img/estadosu.jpg",
        euro: "./img/torree.jpg",
        libra: "./img/inglaterra.jpg",
        rublo: "./img/russia.jpg"
    }

    const imagem = fundos[moeda];
    const box = document.querySelector(".converter-box");

    if (imagem) {
        document.body.style.backgroundImage = `url(${imagem})`;
        document.body.style.backgroundSize = "cover";
        document.body.style.backgroundPosition = "center";
        document.body.style.backgroundRepeat = "no-repeat";
        document.body.style.transition = "background-image 0.5s ease-in-out";
    }

    // Clareia o fundo do conversor
    if (box && !box.classList.contains("ativo")) {
        box.classList.add("ativo");
    }
}

// Toca o hino da moeda selecionada
function tocarHino(moeda) {
    const hinos = {
        real: "./audio/brasil.mp3",
        dolar: "./audio/eua.mp3",
        euro: "./audio/franca1.mp3",
        libra: "./audio/inglaterra.mp3",
        rublo: "./audio/russia.mp3"
    };

    const audio = document.getElementById("audio-hino");
    const hino = hinos[moeda];

    if (hino) {
        audio.src = hino;
        audio.play().catch(err => {
            console.log("Clique do usuário necessário para tocar áudio:", err);
        });
    }
}

// -------------------------------
// FUNÇÃO DE CONVERSÃO
// -------------------------------
function convertValues() {
    const inputValue = document.querySelector(".input-convert").value;

    // Taxas de câmbio fixas
    const realToday = 1.00;
    const dolarToday = 5.56;
    const euroToday = 6.48;
    const gbpToday = 7.60;
    const rubToday = 14.23;

    // -------------------------------
    // CONVERSÃO MOEDA DE DESTINO
    // -------------------------------
    if (selectConvertTwo.value =="dolar") {
        currencyValueTwo.innerHTML = new Intl.NumberFormat("en-US", {
            style: "currency",
            currency: "USD",
        }).format(inputValue / dolarToday);
    }

    if (selectConvertTwo.value =="euro") {
        currencyValueTwo.innerHTML = new Intl.NumberFormat("de-DE", {
            style: "currency",
            currency: "EUR",
        }).format(inputValue / euroToday);
    }

    if (selectConvertTwo.value =="real") {
        currencyValueTwo.innerHTML = new Intl.NumberFormat("pt-BR", {
            style: "currency",
            currency: "BRL",
        }).format(inputValue / realToday);
    }

    if (selectConvertTwo.value =="libra") {
        currencyValueTwo.innerHTML = new Intl.NumberFormat("en-GB", {
            style: "currency",
            currency: "GBP",
        }).format(inputValue / gbpToday);
    }

    if (selectConvertTwo.value =="rublo") {
        currencyValueTwo.innerHTML = new Intl.NumberFormat("ru-RU", {
            style: "currency",
            currency: "RUB",
        }).format(inputValue / rubToday);
    }

    // -------------------------------
    // CONVERSÃO MOEDA DE ORIGEM
    // -------------------------------
    if (selectConvertOne.value =="real") { 
        currencyValueOne.innerHTML = new Intl.NumberFormat("pt-BR", {
            style: "currency",
            currency: "BRL",
        }).format(inputValue / realToday);
    }
  
    if (selectConvertOne.value =="dolar") { 
        currencyValueOne.innerHTML = new Intl.NumberFormat("en-US",{
            style: "currency",
            currency: "USD",
        }).format(inputValue / dolarToday);
    }

    if (selectConvertOne.value =="libra") {
        currencyValueOne.innerHTML = new Intl.NumberFormat("en-GB",{
            style: "currency",
            currency: "GBP",
        }).format(inputValue / gbpToday);
    }

    if (selectConvertOne.value =="rublo") {
        currencyValueOne.innerHTML = new Intl.NumberFormat("ru-RU",{
            style: "currency",
            currency: "RUB",
        }).format(inputValue / rubToday);
    }

    if (selectConvertOne.value =="euro") {
        currencyValueOne.innerHTML = new Intl.NumberFormat("de-DE",{
            style: "currency",
            currency: "EUR",
        }).format(inputValue / euroToday);
    }

    // Troca de background e toca hino
    trocarBackground(selectConvertTwo.value);
    tocarHino(selectConvertTwo.value);
}

// -------------------------------
// FUNÇÕES DE MUDANÇA DE MOEDAS (TEXTOS E IMAGENS)
// -------------------------------
function changeCurrencyTwo() {
    const currencyTwo = document.querySelector(".currency-two");
    const currencyImgTwo = document.querySelector(".currency-img-two");

    if (selectConvertTwo.value == "dolar") {
        currencyTwo.innerHTML = "Dólar americano";
        currencyImgTwo.src = "./img/dolar.png";
    }

    if (selectConvertTwo.value == "euro") {
        currencyTwo.innerHTML = "Euro";
        currencyImgTwo.src = "./img/euro.png";
    }

    if (selectConvertTwo.value == "libra") {
        currencyTwo.innerHTML = "Libra Esterlina";
        currencyImgTwo.src = "./img/libra.png";
    }

    if (selectConvertTwo.value == "real") {
        currencyTwo.innerHTML = "Real Brasileiro";
        currencyImgTwo.src = "./img/real.png";
    }

    if (selectConvertTwo.value == "rublo") {
        currencyTwo.innerHTML = "Rublo Russo";
        currencyImgTwo.src = "./img/rub.svg";
    }
}

function changeCurrencyOne() {
    const currencyOne = document.querySelector(".currency-one");
    const currencyImgOne = document.querySelector(".currency-img-one");

    if (selectConvertOne.value == "dolar") {
        currencyOne.innerHTML = "Dólar americano";
        currencyImgOne.src = "./img/dolar.png";
    }

    if (selectConvertOne.value == "euro") {
        currencyOne.innerHTML = "Euro";
        currencyImgOne.src = "./img/euro.png";
    }

    if (selectConvertOne.value == "libra") {
        currencyOne.innerHTML = "Libra Esterlina";
        currencyImgOne.src = "./img/libra.png";
    }

    if (selectConvertOne.value == "real") {
        currencyOne.innerHTML = "Real Brasileiro";
        currencyImgOne.src = "./img/real.png";
    }

    if (selectConvertOne.value == "rublo") {
        currencyOne.innerHTML = "Rublo Russo";
        currencyImgOne.src = "./img/rub.svg";
    }

    // Atualiza os valores também
    convertValues();
}

// -------------------------------
// EVENT LISTENERS DE CONVERSÃO
// -------------------------------
selectConvertOne.addEventListener("change", changeCurrencyOne);
selectConvertTwo.addEventListener("change", changeCurrencyTwo);
buttonConvert.addEventListener("click", convertValues);

// -------------------------------
// CONTROLES DE ÁUDIO
// -------------------------------
const audio = document.getElementById("audio-hino");
const togglePlayBtn = document.getElementById("toggle-play");
const toggleVolumeBtn = document.getElementById("toggle-volume");

let isPlaying = false;
let isVolumeIncreasing = true;

// Botão Play/Pause
togglePlayBtn.addEventListener("click", () => {
    if (isPlaying) {
        audio.pause();
        togglePlayBtn.textContent = "▶ Play";
    } else {
        audio.play().catch(err => {
            console.log("Clique do usuário necessário para tocar áudio:", err);
        });
        togglePlayBtn.textContent = "⏸ Pause";
    }
    isPlaying = !isPlaying;
});

// Botão de Volume +/- 
toggleVolumeBtn.addEventListener("click", () => {
    if (isVolumeIncreasing) {
        audio.volume = Math.min(1, audio.volume + 0.1);
        toggleVolumeBtn.textContent = "🔊 Volume +";
        if (audio.volume >= 1) isVolumeIncreasing = false;
    } else {
        audio.volume = Math.max(0, audio.volume - 0.1);
        toggleVolumeBtn.textContent = "🔉 Volume -";
        if (audio.volume <= 0) isVolumeIncreasing = true;
    }
    console.log("Volume atual:", audio.volume);
});

// -------------------------------
// MOSTRAR CONVERSOR AO CLICAR NO BOTÃO
// -------------------------------
const startButton = document.getElementById('start-converter');
const hero = document.querySelector('.hero');
const converterBox = document.querySelector('.converter-box');

startButton.addEventListener('click', () => {
    hero.classList.add('hidden');           
    converterBox.classList.remove('hidden'); 
    document.querySelector('.background-overlay').style.opacity = "0.6"; 
});

// -------------------------------
// PARTICULAS NEON DE FUNDO
// -------------------------------
const canvas = document.getElementById('particle-canvas');
const ctx = canvas.getContext('2d');
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

const particles = [];
const particleCount = 100;

for(let i = 0; i < particleCount; i++){
    particles.push({
        x: Math.random() * canvas.width,
        y: Math.random() * canvas.height,
        r: Math.random() * 2 + 1,
        dx: (Math.random() - 0.5) * 0.5,
        dy: (Math.random() - 0.5) * 0.5
    });
}

function animateParticles() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    particles.forEach(p => {
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.r, 0, Math.PI*2);
        ctx.fillStyle = "rgba(0,255,255,0.6)";
        ctx.fill();
        p.x += p.dx;
        p.y += p.dy;
        if(p.x < 0 || p.x > canvas.width) p.dx *= -1;
        if(p.y < 0 || p.y > canvas.height) p.dy *= -1;
    });
    requestAnimationFrame(animateParticles);
}

animateParticles();

window.addEventListener('resize', () => {
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
});
