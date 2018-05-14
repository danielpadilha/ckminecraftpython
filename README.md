# Minecraft Python

## Exemplos

Clique no nome da função para visualizar um exemplo.

<details>
  <summary>
mc.setBlock(x, y, z, block_id, [block_data])
  </summary>

> Set the block at coordinates X/Y/Z to block_id

```python

from mcpi import minecraft

#Connect to minecraft server 127.0.0.1 as player 'steve'
mc = minecraft.Minecraft.create(address="127.0.0.1", name="steve")

#Get current player's position
pos = mc.player.getPos()

#This is the minecraft block ID of the glass block.
#To see what other block IDs are available, go here in your browser: http://minecraft-ids.grahamedgecombe.com/
glass_block_id = 20

#Set the block underneath the player to be glass
mc.setBlock(pos.x, pos.y-1, pos.z, glass_block_id)

#Set the block to the side of player to be wood of a specific subtype
wood_block_id = 5
wood_data = 1 #subtype
mc.setBlock(pos.x+1, pos.y, pos.z, wood_block_id, wood_data)

```

</details>

<details>
  <summary>
mc.getBlock(x, y, z)
  </summary>

> Get the block at coordinates X/Y/Z, returning its block ID

```python

from mcpi import minecraft

# Connect to minecraft server 127.0.0.1 as player 'steve'
mc = minecraft.Minecraft.create(address="127.0.0.1", name="steve")

# Get current player's position
pos = mc.player.getPos()

# Get the block underneath the player
block_id_under_player = mc.getBlock(pos.x, pos.y-1, pos.z)
grass_block_id = 2

if block_id_under_player == grass_block_id:
    print "Player is standing on grass"

```

</details>


<details>
  <summary>
mc.player.getPos()
  </summary>

> Get current player's position exactly (decimals)

```python

from mcpi import minecraft

#Connect to minecraft server 127.0.0.1 as player 'steve'
mc = minecraft.Minecraft.create(address="127.0.0.1", name="bob")

#Get current player's position
pos = mc.player.getPos()

# Returns Vec3(18.3814903971,6.0,25.6063951368)
# Can be accessed as pos.x, pos.y, and pos.z
print pos.x, pos.y, pos.z

```

</details>


<details>
  <summary>
mc.player.setPos(x, y, z)
  </summary>

> Set current player's position exactly (supports decimals)

```python

from mcpi import minecraft

#Connect to minecraft server 127.0.0.1 as player 'steve'
mc = minecraft.Minecraft.create(address="127.0.0.1", name="bob")

#Get current player's position
pos = mc.player.getPos()

#Set current player's position 100 blocks in the air
mc.player.setPos(pos.x, pos.y+100, pos.z)

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

