**Problem**: Who creates object `A`?
**Solution**: In general, Assign class `B` the responsibility to create object `A` if one, or preferably more, of the following apply:
- Instances of `B` contain or compositely aggregate instances of `A`
- Instances of `B` record instances of `A`
- Instances of `B` closely use instances of `A`
- Instances of `B` have the initializing information for instances of `A` and pass it on creation.