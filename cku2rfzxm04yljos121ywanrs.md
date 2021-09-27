## Editando vídeo no terminal com o FFmpeg

## Editar vídeo pelo terminal

- Tirar audio do vídeo
`ffmpeg -i [vídeo com áudio] -c copy -an [vídeo sem áudio]`

Exemplo de como tirar áudio de um vídeo MP4.

`ffmpeg -i video-com-audio.mp4 -c copy -an video-sem-audio.mp4`


- Cortar o video
ffmpeg [tempo inicial] [entrada do vídeo] [duração do corte] [saída do vídeo]

Exemplo: cortar 60 segundos de um vídeo após 1 minuto de vídeo

`ffmpeg.exe -ss 00:01:00 -i "in video-completo.mp4" -to 00:01:00 -c copy video-cortado.mp4`

Para acessar o menu de ajuda digite `ffmpeg -h` ou o manual com mais informações digite `man ffmpeg` no terminal. Eu recomendo a leitura da documentação do [FFMPEG](https://www.ffmpeg.org/ffmpeg-all.html) pois, é possível entender todos os detalhes da ferramenta assim como visualizar exemplos com aplicações reais.

Siga-me nas redes sociais.

[Mayanna Oliveira](https://beacons.ai/mayannaoliveira)