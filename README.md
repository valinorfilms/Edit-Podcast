# CP Multicâmera (Android)

O app de corte multicâmera do Capital Político empacotado como aplicativo Android (.apk), com o Capacitor.

## Como o APK é gerado
O GitHub compila o app sozinho a cada envio para o branch `main`, usando o arquivo `.github/workflows/gerar-apk.yml`. Não é preciso instalar Android Studio.

1. Crie um repositório vazio no GitHub (pode ser privado).
2. Envie esta pasta para ele (o Claude pode fazer isso por você).
3. Na aba **Actions**, acompanhe o "Gerar APK" (leva cerca de 5 minutos).
4. Na aba **Releases**, aparece `CP-Multicamera.apk`.

## Instalar no tablet
1. No tablet, abra a página **Releases** do repositório no Chrome e baixe `CP-Multicamera.apk`.
2. Toque no arquivo baixado. Na primeira vez, o Android pede para **permitir instalar apps desta fonte**: permita para o Chrome.
3. Para atualizar depois, é só baixar o APK novo e instalar por cima. Os dados e ajustes continuam.

## Diferenças em relação à versão web
- **Salvar e enviar XML:** grava o arquivo em `Documentos/CP Multicam/` e abre o menu de compartilhar do Android (Drive, WhatsApp, e-mail…).
- Abre em tela cheia, com ícone próprio, e não depende do link do Claude.

## Mudar o app
O app inteiro está em `www/index.html`. Depois de alterar, envie para o GitHub e um APK novo é gerado.

## Compilar no PC (alternativa)
Com Node 22, JDK 21 e Android Studio instalados:
```
npm ci
npx cap sync android
npx cap open android   # abre no Android Studio: Build > Build APK
```
