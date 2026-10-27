# Zumbis: A Última Cidade — projeto Android

Este projeto empacota o protótipo HTML offline em um aplicativo Android simples usando WebView. O código-fonte está incluído; este pacote ZIP ainda não é um APK compilado.

## Como gerar o APK no Android Studio

1. Instale o Android Studio em um computador e, no SDK Manager, instale Android SDK Platform 35 e uma versão compatível do Android Build Tools.
2. Extraia este ZIP.
3. No Android Studio, escolha **Open** e selecione a pasta `ZumbisUltimaCidadeAndroid`.
4. Aguarde a sincronização do Gradle e aceite a instalação dos componentes solicitados.
5. Para testar no celular: ative as Opções do desenvolvedor e a Depuração USB, conecte o Android e pressione **Run**.
6. Para criar um APK: abra **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
7. O APK de depuração costuma ficar em `app/build/outputs/apk/debug/app-debug.apk`.

## O que está incluído

- Jogo HTML offline dentro do app.
- Tela cheia e orientação horizontal.
- Escolha entre policial e cowboy, movimentação, tiros, zumbis, coleta e barricadas.

## Limitações atuais

- Multiplayer Bluetooth ainda não está implementado.
- É um protótipo inicial; não inclui loja, salvamento de progresso nem sistema completo de armas.
- Para publicar na Play Store, crie uma versão assinada e revise os requisitos atuais do Google Play.

## Compilar sem computador usando GitHub Actions

O projeto inclui o workflow `.github/workflows/build-apk.yml`, que compila o APK na nuvem.

1. No celular, entre em https://github.com e crie uma conta ou faça login.
2. Crie um repositório novo (por exemplo, `zumbis-ultima-cidade`). Selecione **Public** ou **Private** conforme sua preferência.
3. No repositório, use **Add file > Upload files** e envie os arquivos e pastas do projeto extraído. Garanta que `.github/workflows/build-apk.yml` também seja enviado; arquivos começando com ponto podem ficar ocultos no gerenciador de arquivos.
4. Toque em **Commit changes**.
5. Abra a aba **Actions**, selecione **Compilar APK Android** e toque em **Run workflow** se o fluxo não iniciar automaticamente.
6. Quando terminar com sucesso, abra a execução, desça até **Artifacts** e baixe `Zumbis-Ultima-Cidade-APK`.
7. Extraia o ZIP do artefato e toque em `app-debug.apk` para instalar. O Android pode pedir autorização para instalar apps dessa fonte.

O GitHub pode exigir confirmação de e-mail/conta e a compilação depende de os arquivos terem sido enviados corretamente. O APK de depuração serve para teste; não é um pacote assinado para publicação na Play Store.
