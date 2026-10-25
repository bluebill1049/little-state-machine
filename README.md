<div align="center">
  <a href="https://little-state-machine.bluebill1049.dev/" title="Little State Machine">
    <img src="docs/logo.svg" alt="Little State Machine" width="96" />
  </a>
</div>

<p align="center">Simple global state for React.</p>

<div align="center">

[![npm downloads](https://img.shields.io/npm/dm/little-state-machine.svg?style=for-the-badge)](https://www.npmjs.com/package/little-state-machine)
[![npm](https://img.shields.io/npm/dt/little-state-machine.svg?style=for-the-badge)](https://www.npmjs.com/package/little-state-machine)
[![License](https://img.shields.io/npm/l/little-state-machine?style=for-the-badge)](https://github.com/bluebill1049/little-state-machine/blob/master/LICENSE)

</div>

<p align="center">
  <a href="https://little-state-machine.bluebill1049.dev/">Get started</a> |
  <a href="https://little-state-machine.bluebill1049.dev/">Documentation</a> |
  <a href="#quickstart">Quickstart</a>
</p>

### Features

- Tiny, with [no runtime dependencies](./package.json)
- State persistence with session storage by default
- Selectors to limit re-renders

### Install

```sh
npm install little-state-machine
```

### Quickstart

```jsx
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
