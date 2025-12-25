# React
Reactを書くうえでの学びを記す。

## `use`

コンポーネント内で `use` を用いることで、PromiseやContextから値を読み出すことができる。

```tsx
import { fetchData } from '@/api'

const data = useMemo(() => fetchData(), [fetchData])

return (
  {/* `data` が解決されるまで fallback に指定したコンポーネントがレンダリングされる */}
  <Suspense fallback={<Loading />}>
    <DataView {...data}>
  </Suspense>
)
```

```tsx
const DataView = (...props) => {
  const data = use(props)
  return (
    <>
    { /* something ... */ }
    </>
  )
}
```

Suspenseを活用するならアリかも。

```ts
fetchData().then(response => setData(response))
```

みたいなコードを書かなくて良い。