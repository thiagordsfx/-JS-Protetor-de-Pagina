<script>
	(function() {
    // Função para detectar se é um dispositivo móvel com base no User-Agent e no tamanho da tela
    function isMobileDevice() {
        const userAgentMobile = /Mobi|Android|iPhone|iPad|iPod/i.test(navigator.userAgent);
        const screenIsMobile = window.innerWidth <= 768; // Considerando telas de até 768px como mobile
        return userAgentMobile || screenIsMobile;
    }

    // Se não for um dispositivo móvel, execute o código
    if (!isMobileDevice()) {
        // Bloquear logs do console
        console.log = function() {};
        console.warn = function() {};
        console.error = function() {};
        console.info = function() {};
        console.debug = function() {};
        console.table = function() {};
        console.trace = function() {};
        
        // Bloquear atalhos para acessar o código-fonte e ferramentas de desenvolvedor
        document.addEventListener('keydown', function(event) {
            if (event.ctrlKey && event.key.toLowerCase() === 'u') {
                event.preventDefault();
            }
            if (event.ctrlKey && event.shiftKey && (['c', 'j', 'k', 'i'].includes(event.key.toLowerCase()))) {
                event.preventDefault();
            }
            if (['F12', 'F10'].includes(event.key)) {
                event.preventDefault();
            }
            if (event.metaKey && event.altKey && (['u', 'c'].includes(event.key.toLowerCase()))) {
                event.preventDefault();
            }
            if (event.ctrlKey && ['s', 'a', 'c'].includes(event.key.toLowerCase())) {
                event.preventDefault();
            }
        });

        // Bloquear o clique com o botão direito (menu de contexto)
        document.addEventListener('contextmenu', function(event) {
            event.preventDefault();
        });

        // Bloquear a seleção de texto
        document.addEventListener('selectstart', function(event) {
            event.preventDefault();
        });

        // Bloquear o download de imagens
        document.addEventListener("DOMContentLoaded", function() {
            const imagens = document.querySelectorAll('img');
            imagens.forEach(function(imagem) {
                imagem.setAttribute('oncontextmenu', 'return false');
                imagem.setAttribute('draggable', 'false');
            });
        });

        // Detectar ferramentas de desenvolvedor abertas
        (function() {
            let devtoolsOpen = false;
            const threshold = 160;

            function detectDevTools() {
                const widthThreshold = window.outerWidth - window.innerWidth > threshold;
                const heightThreshold = window.outerHeight - window.innerHeight > threshold;

                if (widthThreshold || heightThreshold) {
                    if (!devtoolsOpen) {
                        devtoolsOpen = true; 
                        window.location.href = "https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExYnFwMTNsdmo3MzhobjEwcm54MXY1dGN4N2Uzd3h1MDZhem04YmV0byZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/owRSsSHHoVYFa/giphy.gif"; 
                    }
                } else {
                    devtoolsOpen = false;
                }
            }

            function detectDevToolsByTiming() {
                const start = performance.now();
                debugger;
                const duration = performance.now() - start;
                if (duration > 100) {
                    if (!devtoolsOpen) {
                        devtoolsOpen = true;
                        window.location.href = "https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExYnFwMTNsdmo3MzhobjEwcm54MXY1dGN4N2Uzd3h1MDZhem04YmV0byZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/owRSsSHHoVYFa/giphy.gif"; 
                    }
                } else {
                    devtoolsOpen = false;
                }
            }

            console.log = function() {};
            console.error = function() {};

            setInterval(function() {
                detectDevTools();
                detectDevToolsByTiming();
            }, 2000);
        })();
    }
})();

</script>
