# simple-async-delay

A minimal, awaitable delay utility for JavaScript/TypeScript.

## Install

```bash
npm i simple-async-delay
```

## Usage

```ts
import delay from 'simple-async-delay';

await delay(1000); // pause for 1 second
```

### Sequential delays

```ts
await delay(500);
console.log('step 1');

await delay(500);
console.log('step 2');
```

### In async loops

```ts
for (const item of items) {
  await processItem(item);
  await delay(200); // throttle between iterations
}
```

## API

### `delay(ms: number): Promise<void>`

Returns a Promise that resolves after `ms` milliseconds.

| Parameter | Type     | Description            |
|-----------|----------|------------------------|
| `ms`      | `number` | Delay duration in ms   |

## License

[MIT](./LICENSE)
