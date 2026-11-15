# MeetEase

校园活动的发布与查找平台。活动列表、地图定位、数据存储都在一个应用里。

- Next.js 16（App Router）+ React 19 + TypeScript
- Prisma 6 + libsql：数据库可以是本地 SQLite 文件，也可以是远程实例
- Leaflet / react-leaflet 在地图上标活动地点
- Tailwind CSS 4

## 本地运行

需要 Node.js 20 以上。

```bash
npm install
npx prisma migrate dev   # 建表
npm run dev              # http://localhost:3000
```

数据库地址写在 `.env` 的 `DATABASE_URL`，Prisma 通过 libsql adapter 连接。

## 目录

```text
src/        页面、组件与数据访问
prisma/     schema 与迁移
public/     静态资源
```

## 状态

版本 0.1.0，功能以 `src/` 下实际页面为准。README 不列未验证的完成度，避免写得比代码多。

## 开发约定

改数据库结构先改 `prisma/schema.prisma`，再跑 `npx prisma migrate dev`，不手写建表 SQL。其他约定写在 `AGENTS.md` 和 `CLAUDE.md`，改代码前先读。
