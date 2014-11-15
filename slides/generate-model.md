##  Generator Model / Fixtures


```
jheth@macbook: ~/blog$ ember generate model post
```

```javascript
// app/models/post.js
import DS from 'ember-data';

var Post = DS.Model.extend({
  title: DS.attr('string'),
  body: DS.attr('string'),
  author: DS.attr('string'),
  createdAt: DS.attr('date'),
  isPublished: DS.attr('boolean')
});

Post.reopenClass({
  FIXTURES: [
    { id: 1, title: 'Title A', body: 'Body A', author: 'Joe',
      createdAt: '2014-10-27T11:45:13', isPublished: false },
    { id: 2, title: 'Title B', body: 'Body B', author: 'Paul',
      createdAt: '2014-10-27T12:15:00', isPublished: false }
  ]
});

export default Post;
```
