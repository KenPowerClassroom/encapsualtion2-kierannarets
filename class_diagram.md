```mermaid
classDiagram
    class Shape{
    <<interface>>
    draw(win:Window)
    rotate(angle:float)
    }
    class Square{
      float size
      +area() :float
    }
    class Circle{
      radius:float
    }
    class Figure{
    }
    class Kieran{
    }
    class Colour{
        -r:int
        -g:int
        -b:int
    }
    class Window{
    }

    Square ..|> Shape
    Circle ..|> Shape
    Figure o-- Shape : is made up of
    Kieran .. Shape
    Window -- Kieran
    Shape *-- Colour
    Shape ..> Window
