# API Reference

## Eolic


### Initialize Eolic with an optional list of remote targets.

```py
__init__(self, remote_targets: List[Any]) -> None
```

### Register a new remote target.

```py
register_target(self, target: Any) -> None
```

### Register a new event listener.

```py
register_listener(self, event: Any, fn: Callable[..., None]) -> None
```

### Decorator to register an event listener.

```py
on(self, event: Any) -> Callable
```

### Emit an event to all registered listeners and remote targets.

```py
emit(self, event: Any, *args, **kwargs) -> None
```

## EventRemoteTargetHandler

### Register a remote target.

```py
register(self, target: Any) -> None
```

### Emit an event to all registered remote targets.
```py
emit(self, event: Any, *args, **kwargs) -> None
```

## EventListenerHandler


### Register a new event listener.

```py
register(self, event: Any, fn: Callable[..., None]) -> None
```

### Dictionary mapping events to listeners.

```py
_listener_map
```


## EventRemoteDispatcherFactory


### Create an appropriate dispatcher based on the target type.

```py
create(self, target: EventRemoteTarget) -> EventRemoteDispatcher
```

## EventRemoteURLDispatcher


### Initialize the dispatcher with the given target.

```py
__init__(self, target: EventRemoteTarget) -> None
```

### Dispatch the event to the remote target.

```py
dispatch(self, event: Any, *args, **kwargs) -> None
```