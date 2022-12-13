# Ter visão de esteira de entrega

- "o que a gente precisa agora pra avancar um pouco?"
- 80-20 _rule_

<img alt="Remote Image" src="https://media.briantracy.com/blog/wp-content/uploads/2022/02/04152854/4.png" width="300" height="300"/>

---

# Ter visão de esteira de entrega

O que é importante nessa esteira de entrega?

- Entregar valor
- Pagar débitos técnicos

<br>

<strong>Com isso garantimos que o cliente não vai gastar suas moedas de aposta atoa</strong>

---

# Ter visão de esteira de entrega

O que acontece se fazer um e nao o outro?

- Se você somente pensar em quanto o software "poderia" ser perfeito e bem arquitetado você vai parar de se preocupar com as entregas
- Se você somente entregar _tasks_ nunca vai ter tempo de olhar por um momento o código de forma macro e entender para onde esse Titanic esta nadando

<br><br>
<strong>A chave é equilibrar entre entregar valor e pagar débitos técnicos</strong>

---

# Ter visão de esteira de entrega
### Como tomar decisões

Imagine um sistema:
<br><br>

✓  Crud usuários entregue

🛠 Tarefa de refatoração com 12h


<br><br>

Como explicar essas 12h de trabalho em algo que ja esta entregue?

<!--
o crud de usuario ja foi entregue
ai derrepente o cliente olha que tem mais uma tarefa de refatoracao de usuario com 12h la
ele se pergunta pq tem trabalho nessa task se ela ja tinha sido entregue? como explicar
-->
---

# Ter visão de esteira de entrega
### Como tomar decisões

🥲 Imagine que a causa dessa refatoração é porque o projeto esta usando _repository pattern_ 

🛠 E você tem uma task de para inserir a data de aniversário usuario

<br><br>
<strong>Entregue essa refatoração em pedaços</strong>

<!--
vc precisa refatorar aquilo pra qualidade do projeto continuar (equiliprar entre pagar deb. tecnico e entregar feature)

entregue essa refatoracao aos pedacos, imagine que vc tem uma task de aniversario do usuario. 
esse projeto esta usando repository pattern, aproveita pra refatorar o componente que vc esta usando pra usar a model 
ao invez do repository. nao precisa excluir o repository pattern do projeto inteiro, pq se nao vai dar pau no resto da aplicacao.
mas pelo menos vc deixou o sistema um pouquinho mais a cara da devsquad. e em algum momento vc vai conseguir expurgar aquilo do sistema por completo
-->
---

# Ter visão de esteira de entrega
### Como tomar decisões

- Imagine que tenho uma tarefa pra adicionar um novo campo na tabela de categoria, e varios outras models tem uma categoria associada
- Tambem vamos assumir que essas outras models criadas sao carro e pessoa
- Você olha pra implementacao de categorias e todos os cruds do sistema estao acessando as categorias via repository pattern

<br>

<strong>Você sai alterando todo o sistema?</strong>

<!--
<strong></strong>
agora vamos dizer que tenho uma tarefa pra adicionar um novo campo na tabela de categoria, e varios outras models tem uma categoria associada
e tambem vamos assumir que essas outras models criadas sao carro e pessoa. 
vc olha pra implementacao de categorias e todos os cruds do sistema estao acessando as categorias via repository pattern
vc sai alterando todos esses cruds pra ficar com a carinha da devsquad bonitinho?
-->

---

# Ter visão de esteira de entrega
### Saiba a hora de parar

- Imagina como a esteira de entrega vai ser influenciada pela sua decisão de mudar todo o software para remover esse _pattern_ 
- Seu PR vai tocar em mais arquivos
- Tenho duas models associadas: Pessoa e Carro
  - Vamos assumir que existe um componente Livewire para cada letra do CRUD
  - Ao invés de ter que alterar 3 arquivos(create, read, update) da categoria
  - Você vai ter que alterar 9 arquivos
 
<!--
imagina como a esteira de entrega vai ser influenciada pela sua decisao de mudar todo o software pra remover esse pattern

seu pr vai tocar em mais arquivos, se tenho crud pra pessoa e carro, e vamos assumir que para cada letrinha do crud eu tenho 
um componente livewire seu pr vai tocar em 8 arquivos de crud + crud de categorias.
-->

---

# Ter visão de esteira de entrega
### Saiba a hora de parar

- UM PR que iria tocar apenas no crud de categorias, com apenas modificações pontuais em categorias está com 6 arquivos a mais
- Isso que so relacionei com apenas mais 2 models
- Essa quantidade de arquivos poderíam aumentar exponencialmente se tiver mais models associados
  - A complexidade do PR vai aumentar
  - Vai ser mais custoso para revisar e para fazer o QA

<br><br>

<strong>Por causa do seu PR, agora vai revisar o sistema inteiro?</strong>

<!--
um pr que iria tocar apenas no crud de categorias, com apenas modificacoes pontuais em categorias esta com 12 arquivos a mais
isso que so relacionei com apenas 2 outros models, poderiam ter mais e esse numero cresceria exponencialmente, assim como a complexidade
de revisar e fazer o QA, imagine, por causa do seu pr agora ter que revisar o sistema inteiro?
-->

---

# Combinado não sai caro
### Como organizar

Anote os debitos tecnicos e traga para sprint planning.<br>
Deixe o _decision maker_ ficar ciênte dos problemas.