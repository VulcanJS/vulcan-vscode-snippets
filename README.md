# VulcanJS Snippets

The official Snippets extension for VulcanJS.

## Supported languages

- JavaScript (.js)
- JavaScript React (.jsx)

Support for TypeScript and TypeScript React will be added when the core framework supports it.

## Supported snippets

### `addRoute`

[Docs](http://docs.vulcanjs.org/routing.html#Adding-Routes) | Add a route with a registered component
```js
addRoute({ name: '', path: '/path', componentName: '' });

```

### `addRouteComponent`

[Docs](http://docs.vulcanjs.org/routing.html#Adding-Routes) | Add a route with a direct component
```js
addRoute({ name: '', path: '/path', component:  });

```

### `createCollection`

[Docs](http://docs.vulcanjs.org/schemas.html#Creating-Collections) | Create a collection with custom queries & mutations
```js
const MyDocuments = createCollection({
  collectionName: 'MyDocuments',
  typeName: 'MyDocument',
  schema: mySchema,
  resolvers: myResolvers,
  mutations: myMutations,
});

```

### `createDefaultCollection`

[Docs](http://docs.vulcanjs.org/schemas.html#Creating-Collections) | Create a collection with default queries & mutations
```js
const MyDocuments = createCollection({
  collectionName: 'MyDocuments',
  typeName: 'MyDocument',
  schema: mySchema,
  resolvers: getDefaultResolvers('MyDocument'),
  mutations: getDefaultMutations('MyDocument'),
});

```

### `registerComponent`

[Docs](http://docs.vulcanjs.org/theming.html#Registering-Components) | Register a new component
```js
registerComponent({ name: 'MyComponent', component: MyComponent, hocs: [] });

```

### `registerFragment`

[Docs](http://docs.vulcanjs.org/fragments.html#Registering-Fragments) | Register a new fragment
```js
registerFragment(`
  fragment myFragment on MyType {

  }
`)

```

### `newField`

[Docs](http://docs.vulcanjs.org/schemas.html#Example) | Insert a field inside a schema
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

### `addField`

[Docs](http://docs.vulcanjs.org/schemas.html#Extending-Schemas) | Extend an exisiting collection with a new field
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


### `importvulcancore`

Create an import from `meteor/vulcan:core`
```js
import { } from 'meteor/vulcan:core';
```