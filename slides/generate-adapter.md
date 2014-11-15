##  Generate Adapter


```
ember generate adapter post
version: 0.1.2
installing
  create app/adapters/post.js
installing
  create tests/unit/adapters/post-test.js
```

```
// app/adapters/post.js
import DS from 'ember-data';

export default DS.FixtureAdapter.extend({
});
```
