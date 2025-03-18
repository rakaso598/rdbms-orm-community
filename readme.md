## 목표 : 유저테이블, 게시판테이블, 게시글테이블, 댓글테이블, 좋아요테이블이 있는 프리즈마 ORM을 활용한 PostgreSQL DB CRUD 기능 구현.

![image](https://github.com/user-attachments/assets/fa33d492-b5d8-4b5f-a0d9-6341ba771592)

![image](https://github.com/user-attachments/assets/1afe248d-a75c-4f4c-a44b-3937e494bb29)

- render.com DB 사용함.
- Prisma ORM, 프리즈마 스튜디오 사용함.
- Express 서버 사용함.

---

### postgreSQL 프리즈마 퀵스타트 가이드.

- https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch/relational-databases-typescript-postgresql

---

### render.com의 postgres DB 사용함.

- https://render.com/

---

### 프로젝트 초기화 할때 설치한 것 : npm i express nodemon @types/express cors

---

### 프리즈마

- npx prisma migrate dev
- npx prisma generate
- npx prisma studio

---

- `jsconfig.json` : {} // 루트에 생성, 자바스크립트 기본 설정 사용한다는 의미.

---

- `client.prisma.js` : 프리즈마 클라이언트 사용하도록 만드는 모듈.

---

- 익스프레스에서 json 파싱하려면 : 미들웨어 추가 -> app.use(express.json());

---

- `라우터 기본형`

const express = require("express");

const router = express.Router();

router.메서드("경로", async (req, res, next) => {
try {
console.log("ok")
} catch (e) {
next(e);
}
});

module.exports = router;

---

- `에러처리 미들웨어 기본형`

function errorHandler(err, req, res, next) {
  const statusCode = err.statusCode || 500;
  const message = err.message;

  res.status(statusCode).send(message);
}

module.exports = errorHandler;

---

