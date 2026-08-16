# FP Comprovantes Scanner

Capturador estático de QR para comprovantes FP. Abre a câmera, lê ou recebe por colagem uma URL NFC-e SEFAZ-AM e redireciona o conteúdo codificado à Web App documental.

O decoder operacional único é `@zxing/browser@0.2.1` (MIT), vendorizado em `vendor/`, escolhido após produzir 16/16 leituras idênticas no QR fiscal real. `qr-scanner@1.4.2` permanece apenas como leitura manual no modo diagnóstico; seu resultado detalhado é aceito exclusivamente quando `result.data` é string. Nenhuma imagem é salva ou enviada. A captura manual ZXing tenta um único frame em resolução maior.

Não consulta nem grava planilhas, não autentica usuários, não mantém dados fiscais e não contém credenciais ou lógica econômica. Toda validação de confiança, extração, idempotência e persistência ocorre no backend Apps Script autenticado.

Hospedagem: GitHub Pages, branch `main`, raiz `/`.

## Instalação no iPhone

1. Abra `https://pmcicero.github.io/fp-comprovantes-scanner/` no Safari.
2. Toque em **Compartilhar**.
3. Toque em **Adicionar à Tela de Início**.
4. Confirme o nome **FP Comprovantes** e toque em **Adicionar**.

O ícone abre o scanner em modo standalone. Ao ler um QR, o scanner redireciona para a Web App documental autenticada; o Google poderá solicitar a conta autorizada conforme o estado da sessão do Safari. Na Web App, **Escanear novo comprovante** retorna ao scanner.
