# Vue

## VueX

- A state management system for Vue. Scaling events up and props down can become a problem.
- A single source of truth of data and it is reactive.
- A helpful library of actions, mutations, and getters.

``Vue.use(Vuex)``
``new Vuex.Store(...)``

1. actions -> mutations -> state -> components update
1. **State** - Where the data is stored.
    1. MapState - ?
1. **Getters** - the ability to compute and modify store for ease of use. Can access state.
1. **Mutations** - the ability to mutate state and show state while still being able to store it. To commit and track changes.
    1. ``push(data)``
    1. MapMutation - ?
    1. Ability to rollback state.
    1. Has timestamps.
1. **Actions** - Interacts with mutations and updates state.
    1. ``context.commit(data)``

## Questions

1. Indicators used in apps?
1. How do we rationalize the decisions?

## Resources

1. [Json Server](https://github.com/typicode/json-server)
1. [Vuetify](https://vuetifyjs.com/en/)
