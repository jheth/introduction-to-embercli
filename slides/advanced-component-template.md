##  Advanced Component Template

```
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
```
