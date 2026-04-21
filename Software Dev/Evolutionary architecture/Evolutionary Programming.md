Evolutionary programming is a particular way of writing programs that tries to mimic how real life evolved. Instead of writing an algorithm from the beginning, there's multiple copies of an algorithm run at the same time, with slight variations in their parameters. The ones that [[#Fitness function|perform the best]] are chosen as parents, and new copies are generated from them, adding to the mix some random mutation to their parameters.
# Fitness function
A **fitness function** is a specialized kind of [[Functions|function]] used in **optimization** and **evolutionary algorithms**.
Its purpose is to **evaluate how well a candidate solution meets a goal**—in other words, how "fit" it is.
Like any function, it has a:
- [[Functions#Function definition|Definition]]: specifies _how_ fitness is measured.
- [[Functions#Function invocation|Invocation]]: evaluates a specific solution.
Fitness functions map a candidate (usually a data structure or a set of parameters) to a numeric score. Higher scores mean better solutions.