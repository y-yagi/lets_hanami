### Helpers

```html
<form action="/books" method="POST" accept-charset="utf-8" id="book-form">
  <input type="hidden" name="_csrf_token" value="c5dcffa7fcff2e35ed7e3da2c01ee1c3e8c85c300dc5835c1a134fbe6b47a1af">
  <div class="input">
    <label for="book-title">Title</label>
    <input type="text" name="book[title]" id="book-title" value="">
  </div>
  <div class="input">
    <label for="book-author">Author</label>
    <input type="text" name="book[author]" id="book-author" value="">
  </div>
  <div class="controls">
    <button type="submit">Create Book</button>
  </div>
</form>
```
