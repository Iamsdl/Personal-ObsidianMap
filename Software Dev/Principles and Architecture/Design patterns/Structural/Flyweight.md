**The problem**: You have many instances of objects that have the same value for some fields.

**The solution**: Make those shared fields static so they don't waste memory with each instance.

> This depends on your domain. It's a powerful tool for things like textures or meshes in a video game, but not so much in other areas like web dev where [[Static|static]] is an anti-pattern.