## Shortcut para uma AppImage

### Como configurar
 
1. Faça do download da sua AppImage.
2. Abra o terminal na pasta onde está a AppImage e rode o comando:
```
chmod u+x nome_app.AppImage
```
3. O AppImage deve ter a permição de executar como um programa.
4. Criar shortcut no menu do Ubuntu copie o arquivo abaixo e salve como nome_app.desktop e coloque na pasta **~/.local/share/applications** siga o modelo abaixo:
 
```
[Desktop Entry]
Name=nome_app
Comment=Comentário sobre a aplicação do shortcut
Exec=/home/pasta_usuario/apps/nome_app/nome_app.AppImage
Icon=/home/pasta_usuario/apps/app-icones/nome_icone.png
Terminal=false
Type=Application
Categories=Development
```
 
### Observações:
- Name: nome do programa.
- Comment: comentário curto sobre o programa.
- Exec: Caminho da AppImage.
- Icon: Caminho do ícone para o shortcut.
- Terminal: Rodar terminal sim/não.
- Type: Eu deixo sempre como Application.
- Categories: Nome da categoria.
 
### Modo mais fácil
 
O caminho mais fácil seria instalar um editor de menu como o [AppEditor], [Menu Livre] entre outros e criar via interface gráfica o atalho para executar a AppImage.

![Menu Livre](https://i.imgur.com/e9hEa1f.png)

### Usando o Menu Livre

1. Clique no botão de + para adicionar o shortcut dentro da categoria escolhida (no exemplo é Jogos).
2. Clique em "Novo Lançador" para colocar o nome.
3. Clique no ícone de engrenagem para colocar o ícone da aplicação.
4. Defina o comando ou seja, o caminho onde está a AppImage.
5. Defina um diretório de trabalho.
6. Na área de opções ative ou não: Executar no terminal / Usar notificação de inicialização / Esconder dos menus.
7. Em categorias clique no botão de + e defina a categoria onde será colocado o shortcut.

![Menu Livre](https://i.imgur.com/Kb5yigV.png)

## Problemas com permissões
Caso a haja problemas para rodar o atalho criado da AppImage é recomendável que mude as permissões para 777, siga os passos:
1. Coloque todas as AppImage em uma pasta.
2. Abra o terminal e digite `stat -c  %a minha_pasta` para verificar a permissão.
3 Para trocar a parmissão basta digitar `sudo chmod -R 777 minha_pasta` todas as AppImage dentro da pasta serão executadas sem problemas.


[Menu Livre]: https://launchpad.net/menulibre
[AppEditor]: https://github.com/donadigo/appeditor

*Siga-me nas [redes sociais](https://beacons.ai/mayannaoliveira), eu estarei sempre a disposíção para trocar novas idéias. Sempre que eu puder estarei postando novidades! *

[Mayanna Oliveira]

[Mayanna Oliveira]: https://linktr.ee/mayannaoliveira

