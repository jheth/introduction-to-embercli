##  Generate Routes

```
jheth@macbook: ~/blog$ ember generate route posts
```

```
// app/routes/posts.js
import Ember from 'ember';

export default Ember.Route.extend({
  model: function() {
    return this.store.find('post');
  }
});
```

```
jheth@macbook: ~/blog$ ember generate route post
```

```
// app/routes/post.js
import Ember from 'ember';

export default Ember.Route.extend({
  model: function(params) {
    return this.store.find('post', params.post_id);
  }
});
```

```
// app/router.js
Router.map(function() {
  this.route('posts');
  this.route('post', { path: '/post/:post_id'});
});
```