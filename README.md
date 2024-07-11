# AutoTrack

AutoTrack is a comprehensive web-based application designed to facilitate the management of used car inventories. The system offers intuitive interfaces for both mobile and desktop users, allowing for efficient data collection and manipulation of car inventory. The main features include VIN scanning, automatic car detail retrieval, GPS-based location tracking, photo capturing, and full CRUD (Create, Read, Update, Delete) operations.

## Features

### Mobile Interface for Data Collection
- **VIN Scanning:** Scan the VIN barcode of a vehicle using a mobile device's camera. The system automatically retrieves the car's year, make, and model from a third-party service.
- **Manual Entry:** If automatic retrieval fails, manually enter the year, make, and model.
- **GPS Integration:** Obtain the vehicle's GPS coordinates (latitude and longitude) using the mobile device's GPS sensor.
- **Photo Capture:** Take multiple photos of the vehicle, which are uploaded and stored in the central database.

### Centralized Database
- **Data Storage:** All car details, including VIN, year, make, model, GPS coordinates, and photos, are stored in a centralized MongoDB database.
- **Data Management:** The database supports full CRUD operations, allowing users to create, read, update, and delete car records.

### Desktop and Mobile Interfaces for Inventory Management
- **Inventory Display:** View a list of all cars in the inventory, complete with photos and detailed information.
- **Search and Filter:** Search and filter the inventory based on various criteria such as VIN, make, model, or year.
- **Detailed View:** Each car record displays its VIN, year, make, model, latitude, longitude, and photos.
- **Edit and Delete:** Edit existing car records or delete them from the inventory.

## Technical Implementation

### Backend
- **Server:** Node.js and Express are used to create a robust backend server.
- **Database:** MongoDB is employed for its scalability and flexibility in managing car inventory data.
- **File Uploads:** Multer, a middleware for handling multipart/form-data, is used for photo uploads.
- **VIN Data Retrieval:** Axios is used to interact with third-party APIs to fetch car details based on the VIN.

### Endpoints
- `POST /addCar`: Adds a new car to the inventory, including photos and GPS coordinates.
- `GET /fetchCarDetails/:vin`: Retrieves car details using a VIN.
- `GET /cars`: Fetches all cars from the inventory.
- `GET /car/:id`: Fetches details of a specific car by ID.
- `PUT /car/:id`: Updates the details of a specific car.
- `DELETE /car/:id`: Deletes a specific car from the inventory.

### Frontend
- **Framework:** React.js is used to create a dynamic and responsive user interface.
- **State Management:** React hooks manage the state within the application.
- **GPS Integration:** The Geolocation API is used to obtain GPS coordinates from the user's mobile device.
- **File Handling:** HTML5 file input is used for capturing and handling photo uploads.

## User Workflow

1. **Adding a New Car:**
   - Click the "+" button to get GPS coordinates.
   - Scan the VIN barcode.
   - If available, car details (year, make, model) are auto-filled; otherwise, manually enter them.
   - Capture photos of the car.
   - Submit the form to add the car to the inventory.

2. **Managing Inventory:**
   - Log in to the desktop or mobile interface.
   - View a list of all cars, search, and filter based on criteria.
   - Click on a car to view detailed information and photos.
   - Edit or delete car records as needed.

## Getting Started

### Prerequisites
- Node.js
- MongoDB
- A third-party API key for VIN data retrieval

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/autotrack.git
   cd autotrack
   ```

2. **Install backend dependencies:**
   ```bash
   cd car-inventory
   npm install
   ```

3. **Install frontend dependencies:**
   ```bash
   cd ../car-inventory-frontend
   npm install
   ```

### Running the Application

1. **Start MongoDB:**
   Ensure MongoDB is running on your local machine.

2. **Start the backend server:**
   ```bash
   cd car-inventory
   node server.js
   ```

3. **Start the frontend development server:**
   ```bash
   cd ../car-inventory-frontend
   npm start
   ```

4. **Open the application:**
   Navigate to `http://localhost:3000` in your browser.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License.

---

AutoTrack offers a powerful solution for managing used car inventories, combining modern web technologies with user-friendly interfaces to ensure efficient and accurate data collection and management.
