# FP Comprovantes Scanner

Capturador estático de QR para comprovantes FP. Abre a câmera, lê ou recebe por colagem uma URL NFC-e SEFAZ-AM e redireciona o conteúdo codificado à Web App documental.

O decoder primário é `qr-scanner@1.4.2`. Após 2,5 segundos sem leitura, o scanner ativa localmente o fallback QR-específico `@zxing/browser@0.2.1` (MIT), vendorizado em `vendor/`; nenhuma imagem é salva ou enviada. A captura manual tenta um único frame em resolução maior. A API dos decoders não distingue localização sem decodificação, por isso o diagnóstico usa frames, tempo, FPS e decoder ativo como métricas equivalentes.

Não consulta nem grava planilhas, não autentica usuários, não mantém dados fiscais e não contém credenciais ou lógica econômica. Toda validação de confiança, extração, idempotência e persistência ocorre no backend Apps Script autenticado.

Hospedagem: GitHub Pages, branch `main`, raiz `/`.
