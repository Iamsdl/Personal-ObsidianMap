The problem: You have an inheritance hierarchy that starts evolving in two directions.
>i.e. Shape + Color. Red Triangle, Green Circle.
>If you add a color, you need to write Shape number of classes, If you add a Shape, you need to write Color number of classes

The solution: Turn the relationship from "is a" into "has a".