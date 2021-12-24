# First stackBlitz JS project

> To build a software that your users understand, capture the language of that users in a class diagram.” ― Michael Jesse Chonoles, UML 2 for Dummies.
> [Uml Quotes - Goodreads](https://www.goodreads.com)

```plantuml
@startuml

skinparam  folder {
  BackgroundColor lightgray
}

top to bottom direction
component "Create-project-app" {

  folder "/src" {
    artifact "/..." as src
  }

  folder "/node_modules" {
    artifact "/..." as nodeModules
  }

  folder "/public/..." {
    file "/manifest.json" as manifestLocal
    file "/favicon.ico" as faviconLocal
    file "/index.html" as indexLocal
  }
}

cloud {
  card "localhost:3000" {
  file "main.chunk.js" as mainChunk
  file "vendor~main.chunk.js" as vendorMainChunk
  file "manifest.json" as manifest
  file "favicon.ico" as favicon
  artifact "index.html" as index #white
  file "bundle.js" as bundle
  }
}

src --> mainChunk
nodeModules --> vendorMainChunk
manifestLocal --> manifest
faviconLocal --> favicon
indexLocal --> index

bundle -right-> index
mainChunk -down-> index
vendorMainChunk -down-> index
manifest -down-> index
favicon -down-> index
@enduml
```

UML is **very** ~~convoluted~~ convinient!

|: Name1 |: name2 |
|: ..... |: ..... |
|: val 1 |: val 2 |

![robot-arms](https://www.shutterstock.com/ru/image-vector/isometric-automated-robot-arms-smart-robotic-1106121227 'robot-arms')
