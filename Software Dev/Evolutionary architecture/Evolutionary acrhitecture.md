Some 20-30 years ago when designing a project, the architecture was thought to last. It was planned for 5+ years. But things change and even more so in our current days. 

Evolutionary architecture accepts that change is inevitable and it tries to **guide** the change, aiming to prevent [[bit rot]]. It does this by leveraging a concept from [[Evolutionary Programming]], namely the [[Evolutionary Programming#Fitness function|fitness function]].
The areas where bit rot can occur are called architecture concerns.
## Architecture concerns
After a certain point, a solution is no longer concerned with just the clients' requirements. These concerns are called **architecture concerns** or **cross cutting concerns**, etc. There's many names for them really, but they all boil down to:
-  Auditability
-  Performance
-  Security
-  Requirements
-  Data
-  Legality
-  Scalability
# Fitness function
In **Evolutionary architecture**, a fitness function is any function/metric used to measure how good the solution is.
Fitness functions are categorized based on:
## Scope
- Atomic -> Running against a single concern.
- Holistic -> Running against multiple concerns.
## Cadence
- Triggered -> By events. -> Unit testing, pipeline testing, QA testing.
- Continual -> more like periodic. Constantly checking the system at a particular interval.
- Temporal -> Making sure the code is keeping up with the times by failing older versions if libraries.