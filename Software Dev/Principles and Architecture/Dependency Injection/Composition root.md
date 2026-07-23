Applying [[Dependency Injection]] for all the classes, extracting dependencies out going upwards, you will eventually reach a point where there is no longer an "up", where you have reached the end of the chain. All the dependencies get wired here, and this place is called the Composition Root.
> Usually it sits near or with the starting point of the application

Once everything is wired in the Composition Root, a question arises: how long should each dependency live?

Managing dependencies manually is already enough of a headache, adding lifetime management on top of it will make things very hard to read and follow. As such, we apply [[Indirection]] and extract all this logic into a dedicated class called a [[Dependency Injection Container]].