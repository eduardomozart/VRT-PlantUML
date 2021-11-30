# VRT-PlantUML
Please visit https://www.higithub.com/Piotr1215/repo/sprites, https://crashedmind.github.io/PlantUMLHitchhikersGuide/PlantUMLSpriteLibraries/plantuml_sprites.html and https://plantuml.com/sprite for information on creating and using custom sprites for PlantuML.

The sprites were exported from LibreOffice Draw in PNG format with their default sizes.

## Getting Started

### VSF

![Basic usage - VSF](http://www.plantuml.com/plantuml/proxy?idx=0&src=https%3A%2F%2Fraw.githubusercontent.com%2Feduardomozart%2FVRT-PlantUML%2Fmaster%2Fsamples%2FVSF.puml)

```csharp
@startuml
left to right direction

skinparam {
    ArrowColor Black
    DefaultTextAlignment center
    Shadowing false
}

skinparam rectangle {
    BackgroundColor transparent
    BorderColor #FFFFFF
}

!define VRTPuml https://raw.githubusercontent.com/eduardomozart/VRT-PlantUML/master/dist
!include VRTPuml/Networking/VRTSwitch.puml

rectangle "<color:darkblue><$VRTSwitch{scale=0.51}></color>\n**Access-1 (Master)**" as SW_ACCESS_1
rectangle "<color:darkblue><$VRTSwitch{scale=0.51}></color>\n**Access-2 (Standby)**" as SW_ACCESS_2

SW_ACCESS_1 " 1/1/27" 0-down---0 "1/1/27 " SW_ACCESS_2
@enduml
```
