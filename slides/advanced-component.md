##  Advanced Component

```
export default Ember.Component.extend({
  isEditing: false,
  actions: {
    edit: function() {
      this.set('isEditing', true);
    },
    save: function() {
      this.set('isEditing', false);
    },
    publish: function() {
      this.set('post.isPublished', true);
    },
    unpublish: function() {
      this.set('post.isPublished', false);
    }
  }
});
```
