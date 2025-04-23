# 🏫 School Management API

A Node.js + Express + MySQL REST API to manage schools and find nearby ones using coordinates.

## 🚀 Setup

1. **Clone & install**
```bash
git clone https://github.com/chawlasaksham/SCHOOL-MANAGEMENT-API.git
cd SCHOOL-MANAGEMENT-API
npm install

2. Create .env
MYSQL_HOST=your_host
MYSQL_PORT=your_port
MYSQL_USER=your_user
MYSQL_PASSWORD=your_password
MYSQL_DATABASE=your_db

3. Create MySQL table
CREATE TABLE schools (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255),
  address VARCHAR(255),
  latitude FLOAT,
  longitude FLOAT
);

4. Run
node app.js

5. 📬 API Endpoints

➕ POST /addSchool
Add a school.

Body:

{
  "name": "ABC School",
  "address": "123 St, NY",
  "latitude": 40.7128,
  "longitude": -74.0060
}
Response:

{ "message": "School added successfully", "id": 1 }
📍 GET /listSchools?lat=40.7128&lng=-74.0060
Returns schools sorted by distance.

Response:

[
  {
    "id": 1,
    "name": "ABC School",
    "address": "123 St, NY",
    "latitude": 40.7128,
    "longitude": -74.0060,
    "distance": 0
  }
]
🧪 Postman Collection

🔗 Open in Postman(https://www.postman.com/saksham0204/school-management-api/collection/trcu1ce/school-management-apis?action=share&creator=33444191)

🌍 Deployed on Render

URL: RENDER(https://school-management-api-ivmb.onrender.com)



