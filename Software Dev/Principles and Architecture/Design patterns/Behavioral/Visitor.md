The problem: You have a stable hierarchy of types that keep needing new operations added. Every new operation must be implemented across all types.

The solution: Discriminated Unions if the language permits.

The other Solution: If those operations are "done to" the objects rather than "done by" them, extract them into a dedicated Visitor class. The types only need to know they can be visited, not what the visitor does with them.

