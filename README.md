# OpenCart API Testing

This project contains a Postman collection that tests key API endpoints for the OpenCart Web Application’s **Cart** functionality — including:

- Add Product to Cart
- Edit Cart
- Delete Product from Cart

Tests are implemented directly in Postman’s **Test tab**, using the `Chai.js` assertion library. API requests are chained using variables defined at the **Environment** or **Collection** level.

---
## 🧰 Prerequisites
- Node and npm
- XAMPP and OpenCart Admin Application, *follow instructions from timestamp in this video: [53:00 in this video](https://www.youtube.com/watch?v=5zfgqqPr8o8&t=3180s)*
### 🔧 Install Newman & Reporter

```bash
npm install -g newman
npm install -g newman-reporter-html
```
---

## Usage

### 1. Run in Postman
Simply import the collection into Postman and click **Run**.

### 2. Run via Newman (CLI)

- Step 1: Replace `your_IP` and `your_Port` accordingly:
  ```
  set BASEURL=http://your_IP:your_Port/opencart/upload/index.php?route=
  ```
- Step 2: Run the collection 
  ```
  newman run <collection-name.json> --env-var "baseUrl=%BASEURL%"
  ```
- Step 3: Generate HTML reports
  ```
  newman run <collection-name.json> -r html --env-var "baseUrl=%BASEURL%"
  ```
💡 Note: *`baseUrl`* is an environment variable in Postman. When running collections via Newman, you must manually define it as shown above.

## 📌 Notes: 
- Make sure OpenCart is properly set up and running locally before executing API tests.
- Variables like baseUrl should match your local server setup (e.g., localhost or your IP).
