# VulcanJS Snippets

The official Snippets extension for VulcanJS.

## Supported languages

- JavaScript (.js)
- JavaScript React (.jsx)

Support for TypeScript and TypeScript React will be added when the core framework supports it.

## Supported snippets

### `addRoute`

Add a route with a registered component
```js
addRoute({ name: '', path: '/path', componentName: '' });

```
[Docs](http://docs.vulcanjs.org/routing.html#Adding-Routes)

### `addRouteComponent`

Add a route with a direct component
```js
addRoute({ name: '', path: '/path', component:  });

```
[Docs](http://docs.vulcanjs.org/routing.html#Adding-Routes)

### `createCollection`

Create a collection with custom queries & mutations
```js
const MyDocuments = createCollection({
  collectionName: 'MyDocuments',
  typeName: 'MyDocument',
  schema: mySchema,
  resolvers: myResolvers,
  mutations: myMutations,
});

```
[Docs](http://docs.vulcanjs.org/schemas.html#Creating-Collections)

### `createDefaultCollection`

Create a collection with default queries & mutations
```js
const MyDocuments = createCollection({
  collectionName: 'MyDocuments',
  typeName: 'MyDocument',
  schema: mySchema,
  resolvers: getDefaultResolvers('MyDocument'),
  mutations: getDefaultMutations('MyDocument'),
});

```
[Docs](http://docs.vulcanjs.org/schemas.html#Creating-Collections)

### `registerComponent`

Register a new component
```js
registerComponent({ name: 'MyComponent', component: MyComponent, hocs: [] });

```
[Docs](http://docs.vulcanjs.org/theming.html#Registering-Components)

### `registerFragment`

Register a new fragment
```js
registerFragment(`
  fragment myFragment on MyType {

  }
`)

```
[Docs](http://docs.vulcanjs.org/fragments.html#Registering-Fragments)

### `newField`

Insert a field inside a schema
```js
myFieldName: {
  type: String,
  label: 'MyFieldName',
  optional: true,
  canRead: [],
  canCreate: [],
  canUpdate: [],
},

```
[Docs](http://docs.vulcanjs.org/schemas.html#Example)

### `addField`

Extend an exisiting collection with a new field
```js
.addField({
  fieldName: 'myFieldName',
  fieldSchema: {
    type: String,
    optional: true,
    canRead: [],
    canCreate: [],
    canUpdate: [],
  },
});

```
[Docs](http://docs.vulcanjs.org/schemas.html#Extending-Schemas)

### `importvulcancore`

Create an import from meteor/vulcan:core
```js
import { } from 'meteor/vulcan:core';
```