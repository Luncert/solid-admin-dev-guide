# 通知

本节分享如何使用社区开源轻量化通知组件[solid-toast](https://github.com/ardeora/solid-toast).

1.安装
```shell
npm install --save solid-toast
```

2.添加Toaster组件到布局中

```typescript
// AppLayout.tsx
import { Toaster } from 'solid-toast';

return (
  ...
  <Toaster />
  ...
)
```

3.在子页面中创建toast

```typescript
import toast from 'solid-toast';

toast('消息通知：操作成功')
```