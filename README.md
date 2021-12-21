# Comandos Git
 
1. Iniciando o git
git init

Rodando esse comando na sua pasta será criado um novo repositório local.
Caso essa pasta ja seja um repositório, esse será reiniciado.

2. Trabalhando com Repositório remoto
Repositório remoto consite em um repositorio com serviço de nuvem, o qual o codigo fica armazenado além do repositório local
Exemplos de serviços de nuvem: Github, Gitlab, Bitbucket

2.1 Relacionando repositório local com remoto
git remote add <nome_do_remote> https://github.com/Username/Nome_do_repositório.git
OBS: nome do remote normalmente usado: origin

3. Adicionando/Removendo arquivos da área de preparação
3.1 Adicionando:
git add

Antes de ficar disponível para um commit, os arquivos e/ou pastas do seu repositório precisam ser adicionados ao Git index, ou área de preparação.

O Git index contém as últimas alterações da sua árvore de trabalho antes do próximo commit.

3.1.1 Uso:
Para todas as alterações:
git add .

Para um arquivo específico:
git add <nome_do_arquivo>

Para uma pasta específica:
git add <nome_da_pasta>

3.2 Removendo:
git reset HEAD

O comando reset retorna a zona do buffer para HEAD. Isso limpa a zona do buffer das mudanças que nós acabamos de adicionar ao Git index, ou área de preparação.

3.2.1 Uso:
Para todos os arquivos da área de preparação:
git reset HEAD *

Para um arquivo específico:
git reset HEAD <nome_do_arquivo>

Para uma pasta específica:
git reset HEAD <nome_da_pasta>

4. Área de preparação
git commit -m 'mensagem do commit'

Área de preparação é onde as mudanças feitas nos arquivos que foram adicionados com o git add serão preparadas (Staged changes)

4.1 Atalho
Com o comando abaixo, irá criar um commit com os arquivos marcados como Commit candidate e os modified e junta com a mensagem, mensagem do commit.

git commit -am 'mensagem do commit'

4.2 Histórico de commits
O comando abaixo irá listar os commits feitos no repositório em ordem cronológica inversa. Além disso, esse comando listará cada commit com o seu checksum SHA-1, o nome e email do autor, data de inserção, e a mensagem do commit.

git log

