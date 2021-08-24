
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

### Config
* [ParadoxConfig](https://github.com/RedstoneParadox/ParadoxConfig)
  - config spec defined using delegates
  - supports multiple dataformats, all working with reflection though
* [SpaceServe Config](https://github.com/SpaceServe/spaceserve-config)
  - uses kotlinx.serialization, config spec defined using serializable classes, provides some custom serializers for Minecraft classes
  - supports Json

### Extensions
* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-core)
  - tasks (suspending coroutines and coroutine based), ItemStack builder, Sideboard (Scoreboard) builder, logging, maths (position conversion)
* [Kettle](https://github.com/Cypher121/kettle)
  - tasks (coroutine based), basic Inventory extensions, some extensions for World, Text, Vectors, Boxes etc
* [Kambrik](https://github.com/ejektaflex/Kambrik)

### GUI

#### Server side

* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-igui)
  - server side GUIs using inventories, high a level abstraction, built using a DSL
  - transition effects, automatic rerender on state changes
  - easy to use utilities for listing content 

### Networking
* [Kambrik](https://github.com/ejektaflex/Kambrik)

### NBT Serialization dataformat

All allow the serialization of any serializable class with kotlinx.serialization to an NbtElement. The best NbtElement to represent the input will always be chosen.

* [Fabrik](https://github.com/jakobkmar/fabrikmc) (fabrikmc-nbt)
  - supports nullable types, ignoreUnknownKeys can be set to false, encodeDefaults setting
  - has a reflection fallback if Mixins are not an option
* [Fabric Drawer](https://github.com/natanfudge/Fabric-Drawer)
  - provides serializers for some Minecraft classes
* [Kambrik](https://github.com/ejektaflex/Kambrik)

### Registration

* [Kambrik](https://github.com/ejektaflex/Kambrik)
* [libreg](https://github.com/CursedMC/libreg)

### Serializers
* [KInventory](https://github.com/CmdrNorthpaw/kinventory)
  - allows you to serialize Inventories to any kotlinx.serialization dataformat you want to use

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
