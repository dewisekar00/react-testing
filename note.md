step by step

1. npm install -D vitest
2. in package.json : "test" : "vitest"
3. install testing 
npm i -D jsdom @testing-library/react @testing-library/jest-dom

3.Add this in vite.config.ts

/// <reference types="vitest" />
/// <reference types="vite/client" />

import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  test: {
    globals: true,
    environment:  'jsdom',
    css: true ,
    
  }
})


4.in ts.config.json

    "types": ["vitest/globals"],

5. create file testing
example: App.tes.tsx

6. tambahkan ini   setupFiles: './src/test/setup.ts', di vite.config.ts

7.Buat folder tests di src dan tambah file setup.ts 
dan berisi code import '@testing-library/jest-dom'

Dan mulai untuk test dengan script npm run test