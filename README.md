## Explicação dos Passos no Script
Este script automatiza a criação de pastas, download, descompactação e organização de arquivos em um diretório específico.

1. Criação da pasta com o nome do usuário
O comando mkdir -p "$linux" cria uma pasta com o nome do usuário no diretório atual. A variável $USER armazena o nome de usuário do sistema.

2. Criação da pasta "resultado"
O comando mkdir -p "$linux/resultado" cria uma subpasta chamada "resultado" dentro da pasta com o nome do usuário.

3. Download do arquivo
O comando wget -O "$linux/zip.zip" https://vanilton.net/v1/download/zip.zip faz o download do arquivo zip.zip e o salva na pasta criada com o nome do usuário.

4. Descompactação do arquivo - ## adaptado para Windows
O comando Expand-Archive -Path "$HOME/linux/zip.zip" -DestinationPath $HOME/linux -Force dentro da pasta com o nome do usuário.

5. Movendo os arquivos para a pasta "resultado" - ## adaptado para Windows
O comando Move-Item -Path "C:\Users\wanisia\linux\*.txt" -Destination "C:\Users\wanisia\linux\resultado\" move todos os arquivos descompactados para a pasta "resultado".

6. Remoção do arquivo baixado - ## adaptado para Windows
O comando $linux = "C:\Users\jheni\linux"
Remove-Item -Path "$linux\resultado\zip.zip" remove o arquivo zip.zip que foi baixado.
