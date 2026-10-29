ZUMBIS: A ÚLTIMA CIDADE — estrutura Android

Este pacote contém uma estrutura Android para abrir o jogo HTML dentro de um WebView e compilar um APK pelo GitHub Actions.

IMPORTANTE:
- O arquivo app/src/main/assets/index.html deve conter o HTML completo do jogo.
- O workflow fica em .github/workflows/build-apk.yml.
- A automação usa Gradle instalado no runner, então não precisa do arquivo gradlew.
- Para o GitHub Actions funcionar, os arquivos devem estar nas pastas indicadas no pacote.
- Não apague seu repositório antigo. Faça uma cópia antes de substituir ou mover arquivos.
