
![[Pasted image 20240305185744.png]]

```typescript
type PlusType = (x: number, y: number) => number;

function sum(x: number, y: number): number {
    return x + y;
}

const sum2: PlusType = sum;

```

`PlusType` 是一个函数类型的别名，表示接受两个参数并返回一个数字的函数类型。然后，`sum` 函数符合 `PlusType` 类型的定义，因此你可以将 `sum` 赋值给 `sum2`，这是有效的。

