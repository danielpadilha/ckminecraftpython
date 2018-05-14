# Minecraft Python

## Exemplos

Link para acesso a lista de id dos blocos
http://minecraft-ids.grahamedgecombe.com/

Clique no nome da função para visualizar um exemplo.

<details>
  <summary>
mc.setBlock(x, y, z, bloco_id)
  </summary>

> Criar um bloco do tipo bloco_id na coordenada X,Y,Z

```python


from mcpi.minecraft import minecraft

#Conectar ao servidor 127.0.0.1 com o nome de aluno
mc = Minecraft.create(address="127.0.0.1", name="aluno")

#Obtém a posição atual do jogador
posicao = mc.player.getPos()

#Este é o ID do bloco de vidro
#Para visualizar outros IDs disponiveis entre no site: http://minecraft-ids.grahamedgecombe.com/
bloco_id = 20

#Definir o bloco abaixo do jogador
mc.setBlock(posicao.x, posicao.y-1, posicao.z, bloco_id)

```

</details>

<details>
  <summary>
mc.getBlock(x, y, z)
  </summary>

> Obtém o ID do Bloco que esteja na posição XYZ

```python

from mcpi.minecraft import minecraft

#Conectar ao servidor 127.0.0.1 com o nome de aluno
mc = Minecraft.create(address="127.0.0.1", name="aluno")

#Obtém a posição atual do jogador
posicao = mc.player.getPos()

# Obtém o ID do bloco que esteja abaixo do jogador
id_bloco_abaixo_jogador = mc.getBlock(posicao.x, posicao.y-1, posicao.z)

if id_bloco_abaixo_jogador == id_bloco_grama:
    print "O jogador está sobre a grama"

```

</details>

<details>
  <summary>
mc.player.getTilePos()
  </summary>

> Obtém a posição atual do jogador (número inteiro)

```python

from mcpi.minecraft import minecraft

#Conectar ao servidor 127.0.0.1 com o nome de aluno
mc = Minecraft.create(address="127.0.0.1", name="aluno")

#guardar na variável posicao a posição atual do jogador
posicao = mc.player.getTilePos()

# imprimir a posição x, depois y e por fim z.
print(posicao.x)
print(posicao.y)
print(posicao.z)

```

</details>


<details>
  <summary>
mc.player.setTilePos(x, y, z)
  </summary>

> Definir a nova posição de um jogador. (Somente números inteiros)

```python

from mcpi.minecraft import minecraft

#Conectar ao servidor 127.0.0.1 com o nome de aluno
mc = Minecraft.create(address="127.0.0.1", name="aluno")

#guardar na variável posicao a posição atual do jogador
posicao = mc.player.getTilePos()

#Definir a nova posição do jogador. Neste caso, iremos subir, em Y, 30 unidades do jogador.
mc.player.setTilePos(posicao.x, posicao.y+30, posicao.z)

```

</details>


<details>
  <summary>
mc.postToChat("Hello World!")
  </summary>

> Escrevar qualquer texto no Chat do jogo

```python

from mcpi.minecraft import minecraft

#Conectar ao servidor 127.0.0.1 com o nome de aluno
mc = Minecraft.create(address="127.0.0.1", name="aluno")

mc.postToChat("Olá Pessoal!")

```

</details>

