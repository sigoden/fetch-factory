# fetch 函数工厂

## 开始使用

```js
// 引入
import fetchFactory from "@sigodenjs/fetch-factory"

// 定义
const api = fetchFactory({
  register: ['POST /api/users', 'auth'],
  updateUser: ['PUT /api/user'],
  deleteArticle: ['DELETE /api/articles/:slug'],
  getUser: ['GET /api/articles/:slug'],
}, {
  hooks: {
    auth: () => {

    },
  },
  autoHook: ['reqJson', 'resJson']
});

// 使用接口
const data = await api.register({
  username: "Jacob",
  email: "jake@jake.jake",
  password: "jakejake"
});
```