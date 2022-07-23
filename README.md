# (H1) PDI - Git Fundamentos

## (H2) Repositório
https://github.com/viniciusnyari/pdi_git
Local: C:\temp\pdi_git

### (H3) Curso Udemy
https://www.udemy.com/course/git-e-github-do-basico-ao-avancado-c-gist-e-github-pages/learn/lecture/21981414#overview

#### (H4) Exemplo de H4 (número de hashtag)

##### (H5) Exemplo de H5 (número de hashtag)

###### (H6) Exemplo de H6 (número de hashtag)

Usando **negrito** com dois asteriscos cercando o texto
<br> 
Usando __negrito__ com dois underlines cercando o texto
<br>

Usando *itálico* com um asterisco cercando o texto
<br> 
Usando _italico_ com um underline cercando o texto
<br>

_Combinando o **negrito** e o itálico_
<br>
**Combinando o negrito e o __itálico__**
<br>

### Lista de bullet
* Item 1
* Item 2
* Item 3

### Lista numérica
1. Item 1
2. Item 2
3. Item 3

### Lista usando HTML
<ul>
  <li>1. First Item</li>
  <li>2. Second Item
    <ul>
    <li>2.1 Second Item Sub Item 1 </li>
    <li>2.2 Second Item Sub Item 2</li>
    <li>2.3 Second Item Sub Item 3</li>
    </ul>
  </li>
  <li>3 Third Item </li>
</ul>

## Trabalhando com imagens

#### Inserindo imagem local, do próprio repositório
![Aqui vai a imagem](imagens/GitHub-logo.png)

#### Inserindo imagem externa
![imagem](https://foundations.projectpythia.org/_images/GitHub-logo.png)

## Trabalhando como links

#### Inserindo links como atalho
[Acesse o repositório do PDI_GIT](https://github.com/viniciusnyari/pdi_git)

#### Inserindo links como endereço
[https://github.com/viniciusnyari/pdi_git](https://github.com/viniciusnyari/pdi_git)

#### Inserindo imagem como link
[![Aqui vai a imagem](imagens/GitHub-logo.png)](https://github.com/viniciusnyari/pdi_git)

## Adicionando código javascript
```javascript
function soma(a,b){
   return a+b;
}
```

## Lista de tarefas a fazer
- [x] Concluído 1
- [ ] Pendente 1
- [ ] Pendente 2
- [ ] Pendente 3
- [x] Concluído 2

##### Identificando status de alterações do branch atual
```
git status
```

##### Adiciona todos os arquivos (track)
```
git add .
```

##### Commitando - commitar todos os arquivos (-a) com alguma mensagem (-m)
```
git commit -a -m "mensagem do commit"
```

#####  Enviar para o repositório remoto
```
git push
```

##### Receber todas as alterações de remoto   
```
git pull
```
  
##### Clonando um repositório para a pasta atual  
```
git clone https://github.com/viniciusnyari/pdi_git.git . 
```
  
##### Excluir um arquivo  
```
git rm teste_remover.txt
```
  
##### Exibir histórico - se pressionar q ou ctrl+c sai do modo de log - <enter> vai exibindo os logs 
```
git log - histórico
```

##### Mover o arquivo para outra pasta  
```
git mv mover_esse_arquivo.txt pasta/mover_esse_arquivo.txt
git mv pasta/mover_esse_arquivo.txt pasta2/mover_esse_arquivo_com_outro_nome.txt - movendo arquivo
git mv pasta2/mover_esse_arquivo_com_outro_nome.txt pasta2/arquivo_movido.txt - renomeando arquivo 
```

##### Criar branch e muda para ele
```
git checkout -b <branch-name>
```
  
##### Subir branch para remote
```
git push --set-upstream origin story/67481  
```

##### Clonando branch remoto para a pasta atual
```
git clone https://github.com/viniciusnyari/pdi_git.git .
```

##### Trocar de branch
```
git checkout <nome_branch> - trocar de branch
git switch <nome_branch> - trocar de branch
```

##### Mostrar todos os branchs e qual está selecionada
```
git branch
```

##### Criar uma novo branch
```
git branch <nome branch>
```

##### Desfazendo alterações não commitadas (apenas alteradas) - volta para o original
```
git checkout <nome do arquivo>
```
  
##### Desfazendo alterações commitadas mas não pushadas (reseta ao último push com base no origin/master)
```
git reset -hard  origin/master
git reset -hard  origin/story/67868
```
  
##### Deletando branch
```
git branch segundo_branch -d  
```
  
##### Unindo / merge branches
```
git merge <nome branch>  
```
  
##### Salvar modificações sem commitar e reseta o branch atual para o início
```
git stash  
```
  
##### Listando stash
```
git stash list
```
  
##### Aplicando stash a branch atual - 0 indica a primeira stash listada
```
git stash apply <número da stash>
```

##### Mostrar as alterações de cada stash
```
git stash show -p <número da stash>  
```
  
##### Removendo todas as stash  
```
git stash clear
```

##### Removendo stash específica
```
git stash drop <número stash> 
```
  
##### Criando tags (checkpoint de um branch) - sempre commite as tags - versão 1, versão 2
```
git tag -a <nome> -m "mensagem"
```
  
##### Listando as tags
```
git tag  
```
  
##### Exibindo detalhes da tag
```
git show <nome tag>
```

##### Navegando entre as tags
```
git checkout <nome da tag>  
```
  
##### Enviando uma tag para o repositório remoto
```
git push origin <tag>
```

##### Enviando todas as tags para o repositório remoto
```
git push origin --tags   
```
  
##### Excluindo tag (semelhante ao branch)
```
git tag <nome tag> -d  
```
  
##### Exibindo todos os branchs remotos 
```
git fetch -a  
```
  
##### Submodulos (ter mais de um repositório dentro do mesmo repositório -  um projeto dentro do outro)
```
git submodule add <endereço do outro repositório igual ao clone> <nome da pasta>  
```
  
##### Listando submodulos
```
git submodule 
```

##### Alterando submodule (mesmo esquema de um repositório normal, porém muda o push)
```
git push --recurse-submodules=on-demand  
```
  
##### Identificando diferenças
```  
git diff (exibe diferenças do branch atual para o remoto)
git diff origin/master (exibe diferenças entre atual e outro branch)  
```
  
##### Exibindo logs menores
```
git shortlog
```
  
##### Realiza uma limpeza de arquivos que não estão sendo trackeados (status untrack)
```  
git clean  
git clean -f <força a execução> 
```
  
##### Identifica arquivos que não são mais necessários (otimiza o repositório)
```
git gc  
```
  
##### Checar a integridade e conectividade com o repositório (corrupções de arquivos)  
```
git fsck
```
  
##### Mapeia todos os passos no repositório (exibe tudo o que aconteceu no repositório - mudança de arquivos)
```
git reflog  
pode-se avançar e retroceder commits: git reset --hard <numero do status - b7724cb>
identifica a origem desse branch e os movimentos que aconteceram
```
  
##### Passando o repositório para um arquivo (zipando todos os arquivos do repositório para um arquivo)
```
git archive --format zip --output master_files.zip <branch>  
```
  
##### Alterando informações commitadas (rebase) 
```
git rebase <branch1> <branch2> -i
pick - levar
squash - excluir
reword - alterar o commit
<esc> X! - salva
pressione i para alterar a interação (coloque # na frente do que não quer)
```
  
##### Remover e adicionar arquivo ao gitignore
```
echo debug.log >> .gitignore
git rm --cached debug.log
git commit -m "Start ignoring debug.log"  
```
