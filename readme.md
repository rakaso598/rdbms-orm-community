express, nodemon, @types/express, cors

---

### postgresQL QuickStart Docs

https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch/relational-databases-typescript-postgresql

---

- npx prisma studio
- npx prisma migrate dev
- npx prisma generate

---

- jsconfig.json : {} // 자바스크립트 기본 설정 사용.

---

- client.prisma.js : 프리즈마 클라이언트 사용

---

- 익스프레스에서 json 파싱하려면 : app.use(express.json());

---

const express = require("express");

const router = express.Router();

router.post("/sign-up", async (req, res, next) => {
try {

} catch (e) {
next(e);
}
});

module.exports = router;

---

function errorHandler(err, req, res, next) {}

module.exports = errorHandler;
