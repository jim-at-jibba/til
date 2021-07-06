# Match current route in React Router

There are time where you might want to match your current route and perform an action of the back of the match being truthy e.g to perform analytics event

The best way I have found is to use `useRouteMatch`

```javascript

const routeMatch = useRouteMatch(`/test/route/:id`);

if (routeMatch != null && routMoute.isExact) {
  // perform some action
}
```
