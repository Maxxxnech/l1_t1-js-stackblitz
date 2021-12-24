# First stackBlitz JS project

> To build a software that your users understand, capture the language of that users  in a class diagram.” ― Michael Jesse Chonoles, UML 2 for Dummies.
[Uml Quotes - Goodreads](https://www.goodreads.com)

![create-react-app diagram](https://plantuml-server.kkeisuke.dev/svg/VLF1JiCm3BtdAwnoRfd4ZGEQs9Lz0ygITCsMs5MIRY0qlfqqMKlNCYwLxFVy_6odQn-u2vqrZFcZnfOxRW5gCb8v-680hrmSzuuwb1iovC3eVHFsZd-o2sE1MWW4Emg1B4Zjb0YQa0coBQ720CN6AHvKsJewHB3aRLj4NJRsA1wz4qLg1H2jw9gBMFPOLLK1t4D48tIvgK2IwjsIx8po_vJsj6rcBIJQRcUqoDGiK6kZ8c0vwbhvK1qyOP8PCcyak9bIQtxIWh2AdqIynWkUHga-gYPOasWf74YNVet2K2UJ3S6TXCBqO4C-F3-jLgjiC6jPhh4IJOV7wE_gJkEcJuoSaq99xdj9pS1sKN1_v95oPrGstVjVOyB3kT51ZJgx-8wC6WpbQDX2l3IKPVao6MboGUYH-GGtfu5SUtK-FKP21ik_wy_TKinOzWAbwz_tc1wjG2dfZ6D-PcI63YPcwQk3MNOTfUB_zmC0.svg "create-react-app")

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

src ---> mainChunk
nodeModules --> vendorMainChunk
manifestLocal --> manifest
faviconLocal --> favicon
indexLocal ---> index

bundle -right-> index
mainChunk -down-> index
vendorMainChunk -down-> index
manifest -down-> index
favicon -down-> index
@enduml

```

UML is **very** ~~convoluted~~ convinient!

| Attribute           | AngularJS      | Angular 2  | React    |
| :------------------ | :------------: | :--------: | --------:|
| Author              | Google         | Google     | Facebook |
| Language            | JavaScript/HTML| TypeScript | JSX      |
| Size                | 143k           | 764k       | 151k     |
| Github Stars        | 46.4k          | 8.4k	    | 34.4k    |
| Github Contributors |	1,386	       | 189	    | 604      |

![robot-arms](https://image.shutterstock.com/shutterstock/photos/1106121227/display_1500/stock-vector-isometric-automated-robot-arms-smart-automated-robotic-arms-holding-box-in-a-warehouse-modern-1106121227.jpg "robot-arms")

 
