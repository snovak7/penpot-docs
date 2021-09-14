---
title: 3bis. Data model
---

# Data model

Definition of file

@startuml DataModel

class File
class Page
class Component
class Color
class MediaItem
class Typography

File *-- "*" Page : pages
(File, Page) .. PagesList

File *-- "*" Component : components
(File, Component) .. ComponentsList

File *-- "*" Color : colors
(File, Color) .. ColorsList

File *-- "*" MediaItem : colors
(File, MediaItem) .. MediaItemsList

File *-- "*" Typography : colors
(File, Typography) .. TypographysList

@enduml

Definition of shapes

@startuml DataModel

class Container
class Page
class Component
class Shape

Container <|-left- Page
Container <|-right- Component

Container *-- "*" Shape : objects
(Container, Shape) .. ShapeTree

@enduml
