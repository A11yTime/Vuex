# vuex-app

## Install vuex --> npm install vuex@next --save
#### Terminology:
* State: The data you store in Vuex follows the same rules as the data in a Vue instance
* Getters: Sometimes we may need to compute derived state based on store state
* Mutations: Vuex mutations are very similar to events
* Actions: Actions are similar to mutations, the differences being that:
     * Instead of mutating the state, actions commit mutations.
     * Actions can contain arbitrary asynchronous operations.
* Moudules: Vuex allows us to divide our store into modules
