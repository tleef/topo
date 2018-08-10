# topo

Topological sorting with grouping support.

![npm (scoped)](https://img.shields.io/npm/v/@tleef/topo.svg)
![Travis (.org) branch](https://img.shields.io/travis/tleef/topo/release.svg)
![Coveralls github branch](https://img.shields.io/coveralls/github/tleef/topo/release.svg)

Lead Maintainer: [Devin Ivy](https://github.com/devinivy)

## Usage

See the [API Reference](API.md)

**Example**
```node
const Topo = require('topo');

const morning = new Topo();

morning.add('Nap', { after: ['breakfast', 'prep'] });

morning.add([
    'Make toast',
    'Pour juice'
], { before: 'breakfast', group: 'prep' });

morning.add('Eat breakfast', { group: 'breakfast' });

morning.nodes;        // ['Make toast', 'Pour juice', 'Eat breakfast', 'Nap']
```
