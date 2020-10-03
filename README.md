# Async Function

## Description

The purpose of async/await is to simplify the syntax necessary to consume promise-based APIs.

## Example

### API

Request:

```http
GET https://mywebsite.cc/api/foo
```

Response:

```plaintext
foo
```

### Promise Chaining Sample

```js
function foo() {
  fetch("https://mywebsite.cc/api/foo")
    .then((responseObj) => responseObj.text())
    .then((content) => console.log(content));
}
```

After the promise returned by `fetch` is fulfilled, the promise invokes the callback function (defined in the first `then`) with taking the result of that promise as its argument.

### Using Async Function

```js
async function foo() {
  const responseObj = await fetch("https://mywebsite.cc/api/foo");
  const content = await responseObj.text();
  console.log(content);
}
```
