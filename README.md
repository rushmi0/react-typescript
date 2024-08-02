# React + TypeScript + Vite + Tailwind CSS + daisyUI


### เอกสารข้อมูลเพิ่มเติม
 - [Tailwind CSS](https://tailwindcss.com/docs/guides/vite)
 - [daisyUI](https://daisyui.com/docs/install/)

## ขั้นตอนติดตั้ง Tailwind CSS + daisyUI

เปิด Terminal แล้วรันคำสั่งชุดนี้

```shell
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
npm i -D daisyui@latest
```

สร้างไฟล์กำหนดค่า `tailwind.config.js` แล้วเพิ่มเนื้อหาดังนี้

```js
/** @type {import('tailwindcss').Config} */
export default {
    content: [
        "./index.html",
        "./src/**/*.{js,ts,jsx,tsx}",
    ],
    theme: {
        extend: {},
    },
    plugins: [
        require('daisyui'),
    ],
    daisyui: {
        themes: [false],
    },
}
```

ปรับแก้ไขเนื้อหาทั้งหมดที่ `./src/index.css`แล้วแทนที่ด้วยคำสั่งชุดนี้

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```