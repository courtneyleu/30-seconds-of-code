---
title: Model
tags: model, NodeJS
expertise: intermediate
firstSeen: 2021-06-13T05:00:00-04:00
---

Creates backend API models.

- Input all fields of your model with correct type.
- Connects other models to this model.

```js
const mongoose = require("mongoose");

const modelNameSchema = new mongoose.Schema({
  differentModelID: {
    type: mongoose.Schema.ObjectId,
    ref: "differentModel",
  },
  anotherField: {
    type: String,
    trim: true,
  },
});
```

```js
const mongoose = require("mongoose");

const classSchema = new mongoose.Schema({
  teacherID: {
    type: mongoose.Schema.ObjectId,
    ref: "teacher",
  },
  className: {
    type: String,
    trim: true,
  },
  numStudents: {
    type: Number,
    trim: true,
  },
});
```
