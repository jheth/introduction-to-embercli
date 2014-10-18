##  Generate Controller

```
jheth@macbook: ~/blog$ ember generate controllers posts --type=array
```

```
import Ember from 'ember';

export default Ember.ArrayController.extend({
  actions: {
    createPost: function() {
      this.store.createRecord('post', {
        id: Math.floor((Math.random() * 100) + 1),
        title: this.get('title'),
        body: this.get('body'),
        author: this.get('author'),
        createdAt: new Date().toISOString(),
        isPublished: false
      });

      this.set('title', '');
      this.set('body', '');
      this.set('author', '');
    },
    deletePost: function(post) {
      post.destroyRecord();
    }
  }
});
```