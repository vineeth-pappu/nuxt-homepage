Services folder include api services decoupled from store actions.
Component/Page will dispatch action -> action will call the service -> after receiving data, action will commit to store.
