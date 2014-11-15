##  Update Templates

```
// app/templates/application.hbs

{{link-to 'Posts' 'posts'}}

```

```
// app/templates/post.hbs

{{blog-post post=model}}

{{outlet}}
```

```
// app/templates/posts.hbs

<h1>My Blog ({{controller.length}})</h1>
{{#each}}
  <h1>{{#link-to 'post' this }}{{title}}{{/link-to}}</h1>
  Created by {{author}} on {{createdAt}}
  {{#if isPublished}}
    <strong>PUBLISHED</strong>
  {{/if}}
  <hr>
{{/each}}

```

Note:

<br>
<a href="#" {{action 'deletePost' this }}>Delete Post</a>


<h2>New Post</h2>
Title: {{input type='text' value=title}}<br>
Body: {{textarea value=body}}<br>
Author: {{input type='text' value=author}}<br>
<button {{action 'createPost'}}>Save</button>

{{outlet}}
