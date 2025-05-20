```css
div:has(input:checked) {
  background-color: lightgreen;
}
```

# If a div contains a checked `<input>,` change its background.

`
`
`
`
`
`
`
`

```css
@container (min-width: 500px) {
  .card {
    flex-direction: row;
  }
}
```

# This is called `@container` Queries

### 🧠 What is @container in CSS?

##### `@container` is like `@media`, **but smarter** — instead of reacting to the whole screen's size, it reacts to the size of a container element.

##### It’s perfect for responsive components that live inside other layouts.

### 💡 Meaning:

##### If the container holding .card is 600px or wider, then apply the styles inside.

### 🔁 Comparison: `@media` vs `@container`

| Feature       | `@media`                      | `@container`                      |
| ------------- | ----------------------------- | --------------------------------- |
| Reacts to...  | **viewport** (browser window) | **element/container size**        |
| Use for...    | Full-page layout changes      | Component-specific responsiveness |
| Where to use? | At root level                 | Inside components/modules         |

### ✅ How to Use @container Step-by-Step

### 🔹 1. Set `container-type` on the parent

```css
.card-wrapper {
  container-type: inline-size;
}
```

#### 🔹 2. Use `@container` to write rules

```css
@container (min-width: 500px) {
  .card {
    flex-direction: row;
  }
}
```

### 🔥 Why Is This So Useful?

#### With @container, your components become responsive on their own, without depending on the full page size. It's a game-changer for building modular, reusable components.

`
`
`
`
`
`

# CSS Nesting

#### CSS Nesting lets you write CSS rules inside other rules, so you can keep related styles grouped together.

```css
.card {
  padding: 1rem;

  img {
    width: 100%;
  }

  &:hover {
    background-color: #f9f9f9;
  }
}
```

## Pseudo-classes

```css
.button {
  color: white;

  &:hover {
    background: black;
  }
}
```

## Media Queries Inside

```css
.card {
  padding: 20px;

  @media (max-width: 600px) {
    padding: 10px;
  }
}
```

## Using & for Parent Reference

```css
.btn {
  &.primary {
    background: blue;
  }

  &.danger {
    background: red;
  }
}
```

| Feature           | What it does                          |
| ----------------- | ------------------------------------- |
| Nesting Selectors | Keep related styles inside a parent   |
| `&` Symbol        | Refers to the parent selector         |
| Pseudo-classes    | Use inside `&:hover`, `&:focus`, etc. |
| Media queries     | Can be written inside a block         |
