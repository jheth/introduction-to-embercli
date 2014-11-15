##  Generate Component

```
jheth@macbook: ~/blog$ ember generate components blog-post
version: 0.1.2
installing
  create app/components/blog-post.js
  create app/templates/components/blog-post.hbs
installing
  create tests/unit/components/blog-post-test.js
```

```
<div class="post">
<h1>{{post.title}}</h1>
<p>{{post.body}}</p>
</div>
```

Note:

<div class="post">
  {{#if isEditing}}
    <h1>{{input type='text' value=post.title}}</h1>
    {{textarea value=post.body}}
    <br>
    <button {{action 'save'}}>Save</button>
  {{else}}
    <h1>{{post.title}}</h1>
    {{post.body}}
    <br>
    <button {{action 'edit'}}>Edit</button>

    {{#if post.isPublished}}
    <button {{action 'unpublish'}}>Unpublish</button>
    {{else}}
    <button {{action 'publish'}}>Publish</button>
    {{/if}}
  {{/if}}
</div>
