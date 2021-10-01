## Visual Studio Code diretamente do navegador

## Tutorial de como usar o  OpenVSCode Server

Navegando pelo Github encontrei um repositório com um projeto maravilhoso, porque não rodar o Visual Studio Code diretamente do navegador? Isso só é possível graças ao projeto [OpenVSCode Server]. Abaixo o vídeo da [Gitpod] demostrando como executar o [OpenVSCode Server]:

[![Launching OpenVSCode server ](https://res.cloudinary.com/marcomontalbano/image/upload/v1632884004/video_to_markdown/images/youtube--qGR7rgqjdiY-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=qGR7rgqjdiY&t=1s "Launching OpenVSCode server ")

Como rodar o Visual Studio Code diretamente do navegador:
1. Ter o Docker devidamente instalado. Caso precise de ajuda na instalação do [Docker] eu recomendo a leitura da documentação [Install Docker Engine on Ubuntu], [Install Docker Desktop on Mac] ou [Install Docker Desktop on Windows].
2. Crie uma pasta e abra o terminal dentro da pasta criada. Via terminal com o comando `mkdir vscode-docker && cd vscode-docker`.
3. Digite no terminal `docker run -it --init -p 3000:3000 -v "$(pwd):/home/workspace:cached" gitpod/openvscode-server` caso peça permissão de administrador rode `sudo  docker run -it --init -p 3000:3000 -v "$(pwd):/home/workspace:cached" gitpod/openvscode-server`. Aguarde a instalação dos pacotes.
4. Após a conclusão abra o navegador no endereço `http://0.0.0.0:3000`. Agora é só usar o OpenVSCode.
5. Caso precise instalar extensões busque por elas no [Extensions for VS Code Compatible Editors].
6. Para usar no Github é só colocar o link `https://gitpod.io/#` antes da URL do repositório. Exemplo: `https://gitpod.io/#[URL do repositório]` ou seja, `https://gitpod.io/#https://github.com/mayannaoliveira/repositorio-de-testes`.

%[https://github.com/gitpod-io/gitpod]

Caso você queira conhecer mais sobre o Gitpod eu recomendo a série de vídeos abaixo: 
[![Gitpod Screencast 01: Getting started with Gitpod](https://res.cloudinary.com/marcomontalbano/image/upload/v1632884137/video_to_markdown/images/youtube--w65POyu3ZUQ-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=w65POyu3ZUQ&t=117s "Gitpod Screencast 01: Getting started with Gitpod")

[![Gitpod](https://shields.io/badge/Playlist%20no%20Youtube-Gitpod%20Screencast-red?logo=youtube&style=for-the-badge)](https://youtu.be/w65POyu3ZUQ)

Caso você tenha interesse de saber mais sobre a integração do [Gipod com o Gitlab] só acessar a documentação onde tem o passo a passo de como usar a ferramenta.

#### Referências
[Documentação do Docker], [Repositório do Gitpod], [Documentação do Gitpod], [Gitpod], [Open VSX], [OpenVSCode Server], [Docker], [Install Docker Desktop on Mac], [Install Docker Engine on Ubuntu] e [Install Docker Desktop on Windows]. 

[Extensions for VS Code Compatible Editors]: https://open-vsx.org/
[Gitpod]: https://www.gitpod.io/blog/openvscode-server-launch
[OpenVSCode Server]: https://github.com/gitpod-io/openvscode-server/
[Docker]: https://docs.docker.com/desktop/
[Install Docker Desktop on Mac]: https://docs.docker.com/desktop/mac/install/
[Install Docker Engine on Ubuntu]: https://docs.docker.com/engine/install/ubuntu/
[Install Docker Desktop on Windows]: https://docs.docker.com/desktop/windows/install/
[Open VSX]: https://open-vsx.org/
[Documentação do Gitpod]: https://www.gitpod.io/docs
[Repositório do Gitpod]: https://github.com/gitpod-io/gitpod
[Documentação do Docker]: https://docs.docker.com/
[Gipod com o Gitlab]: https://docs.gitlab.com/ee/integration/gitpod.html 


Seu apoio é importante então siga, compartilhe e curta.


por [Mayanna Oliveira](https://beacons.ai/mayannaoliveira)


| ![testado no firefox](https://img.shields.io/badge/Tutorial%20testado%20no-Firefox-red?style=for-the-badge&logo=firefox&logoColor=white) |  ![testado no brave](https://img.shields.io/badge/Tutorial%20testado%20no-Brave-orange?style=for-the-badge&logo=brave&logoColor=white) | ![testado no linux lite](https://img.shields.io/badge/Tutorial%20testado%20no-Linux%20Lite-FCC624?style=for-the-badge&logo=linux&logoColor=white) |
|---|---|---|
| [![gitpod](https://img.shields.io/badge/Disponível%20pelo-gitpod-yellow?style=for-the-badge&logo=gitpod&logoColor=white)](https://www.gitpod.io/blog/openvscode-server-launch) | [![precisa do docker](https://img.shields.io/badge/Precisa%20do-Docker-blue?style=for-the-badge&logo=docker&logoColor=white)](https://docs.docker.com/desktop/) | [![open vsx](https://img.shields.io/badge/Extensões%20via-Open%20VSX-blue?style=for-the-badge&logo=Visual%20Studio%20Code&logoColor=white)](https://open-vsx.org/) |
