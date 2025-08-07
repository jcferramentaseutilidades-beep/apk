
# Alternador de Links (APK a partir do seu HTML)

Este projeto Android carrega seu arquivo `alternador_links.html` em um WebView e alterna os relatórios a cada 15s.

## Como gerar o APK (passo a passo rápido)
1. **Baixe o ZIP** deste projeto e extraia.
2. Abra o Android Studio (Giraffe/Koala ou mais novo) > **Open** > selecione a pasta `AlternadorLinksAndroid`.
3. Aguarde o *Gradle Sync* concluir (o Android Studio baixará o que faltar).
4. Menu **Build** > **Build Bundle(s) / APK(s)** > **Build APK(s)**.
5. O APK de *debug* ficará em `app/build/outputs/apk/debug/app-debug.apk`.
   - Para publicar/instalar amplamente, gere um **APK assinado**: **Build** > **Generate Signed Bundle / APK**.

## Dicas/Permissões
- O app já inclui a permissão de **INTERNET** para abrir os relatórios (HTTPS) dentro do iframe.
- O WebView tem **JavaScript** e **DOM Storage** habilitados.
- Caso a Zoho exija autenticação, você precisará estar logado no dispositivo ou usar *links públicos*.

## Ajustes rápidos
- Para mudar os links ou o tempo, edite `app/src/main/assets/alternador_links.html`:
  - `links = [ ... ]`
  - `tempoTroca = 15000` (em ms)
