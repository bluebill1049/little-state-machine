<div align="center">
  <a href="https://little-state-machine.bluebill1049.dev/">
    <img src="docs/logo.svg" alt="Little State Machine" width="96" />
  </a>

  # Little State Machine

  Simple global state for React.
</div>

## Features

- Tiny, with no runtime dependencies
- State persistence with session storage by default
- Selectors to limit re-renders

## Install

```bash
npm install little-state-machine
```

## Quickstart

```tsx
import { createStore, useStateMachine } from 'little-state-machine';

createStore({ count: 0 });

function increment(state) {
  return { ...state, count: state.count + 1 };
}

function Counter() {
  const { actions, state } = useStateMachine({ actions: { increment } });

  return <button onClick={() => actions.increment()}>{state.count}</button>;
}
```

Read the [documentation](https://little-state-machine.bluebill1049.dev/) for options, selectors, and TypeScript setup.
