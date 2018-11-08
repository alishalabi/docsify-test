# Testing Docsify: Holy Me-Mo-My

Section 1: Highlighting Javascript

Sample Routes From SPD1.2 Project:

```js
//HTTP Request: Index
app.get("/phrases", (req, res) => {
  Phrase.find()
    .then(phrases => {
      res.render("phrases-index", { phrases: phrases });
    })
    .catch((err) => {
      console.log(err.message);
    })
})```


```js
//HTTP Request: Show
app.get("/phrases/:id", (req, res) => {
  Phrase.findById(req.params.id)
    .then((phrase) => {
      res.render("phrases-show", { phrase: phrase })
    })
    .catch((err) => {
      console.log(err.message);
    })
})```
