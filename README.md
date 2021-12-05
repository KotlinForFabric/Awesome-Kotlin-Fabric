
# Awesome Kotlin for Fabric

Here are some Kotlin libraries for Fabric, and the 1.17.x versions of Minecraft!

Categories are listed alphabetically. 

Libraries are listed roughly in order of followers.

### Command DSL / Builders

* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-commands)
  - provides extensions for the Brigardier classes, without wrapping anything
  - no duplicated argument names as strings needed for getting the argument value
* [Aegis](https://github.com/P03W/Aegis)
  - wraps Brigardier with its own command builder (still allows you to access raw Brigardier though)
  - argument types are defined via the function name
* [Kambrik](https://github.com/ejektaflex/Kambrik)
  - offers an alternative command DSL that exists on top of Brigadier

### Config
* [ParadoxConfig](https://github.com/RedstoneParadox/ParadoxConfig)
  - config spec defined using delegates
  - supports multiple dataformats, all working with reflection though
* [SpaceServe Config](https://github.com/SpaceServe/spaceserve-config)
  - uses kotlinx.serialization, config spec defined using serializable classes, provides some custom serializers for Minecraft classes
  - supports Json
* [Kambrik](https://github.com/ejektaflex/Kambrik)
  - Kambrik's persistance api provides a great way of persisting data between launches
  - easily link variables to a config instance using delegation
  - config entries can exist between multiple files for ultimate flexibility

### Extensions
* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-core *and* fabrikmc-game)
  - in core module: tasks (suspending coroutines and coroutine based), ItemStack builder, logging, maths (position conversion)
  - in game module: sideboard (Scoreboard) builder, cooldown API
* [Kettle](https://github.com/Cypher121/kettle)
  - tasks (coroutine based), basic Inventory extensions, some extensions for World, Text, Vectors, Boxes etc
* [Kambrik](https://github.com/ejektaflex/Kambrik)

### GUI

#### Server side

* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-compose)
  - render any compose gui on the server side and display it to the player ingame
  - gives you acces to the whole world of Material UI
  - more info on compose can be found [here](https://github.com/JetBrains/compose-jb)
* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-igui)
  - server side GUIs using inventories, high level abstraction, GUI built using a DSL
  - transition effects, automatic rerender on state changes
  - easy to use utilities for listing content 

### Networking
* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-network)
  - allows you to send any serializable class as packets
  - uses cbor
  - supports s2c, c2s, c2c (over server)
* [Kambrik](https://github.com/ejektaflex/Kambrik)
  - allows you to send any serialzable class as packets
  - uses json
  - supports s2c and c2c (over server)

### NBT Serialization dataformat

All allow the serialization of any serializable class with kotlinx.serialization to an NbtElement. The best NbtElement to represent the input will always be chosen.

* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-nbt)
  - supports nullable types, ignoreUnknownKeys can be set to false, encodeDefaults setting
  - has a reflection fallback if Mixins are not an option
* [Fabric Drawer](https://github.com/natanfudge/Fabric-Drawer)
  - provides serializers for some Minecraft classes
* [Kambrik](https://github.com/ejektaflex/Kambrik)
  - can convert any kotlin class to nbt similar to how gson converts java objects to json. see category description

### Registration

* [Kambrik](https://github.com/ejektaflex/Kambrik)
  - allows easy registration for most minecraft registry types
  - uses infix functions for super-clean syntax
* [libreg](https://github.com/CursedMC/libreg)

### Serializers

All allow you to target any kotlinx.serialization dataformat you want to use.

* [KInventory](https://github.com/CmdrNorthpaw/kinventory)
  - allows you to serialize Inventories

### Storage

* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-persistence)
  - allows you to store any serializable class and all primitives to component holders such as Chunks, Entities and so on
  - fast in memory access and storage, will be stored persistently when the game is saved

### Text DSL / Builders

* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-core)
  - makes sure that components do always work, even with the weirdest combinations
* [SpaceServe Ekho](https://github.com/SpaceServe/spaceserve-ekho)
  - can be the shortest
* [Kambrik](https://github.com/ejektaflex/Kambrik)
