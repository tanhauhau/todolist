# todolist

## Background

After listened to [Thai Pangsakulyanont](https://twitter.com/dtinth)'s [talk in JSConfAsia 2019, Race Conditions in JavaScript Apps](https://twitter.com/jsconfasia/status/961088327867944961), I realised there's so many different edge cases in the async world that I have never thought of before. So the following is my homework project, to build something simple like [TodoMVC](https://github.com/tastejs/todomvc) with Optimistic UI and async edge case handling.

So the following is the list of edge cases I will have to handle:
- Out of order promise resolves
- Debounce
- Retry: Exponential Backoff
- Cancellable actions
  - Create a process that takes a few async calls, eg: create a image todo (upload thumbnail, updates thumbnail url, create todo)
  - User is allow to cancel at anytime throughout the process
- Batched operations
  - Taking care of dependencies of the operation
- Offline background sync
