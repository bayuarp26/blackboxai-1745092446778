
Built by https://www.blackbox.ai

---

```markdown
# User Workspace - Location Tracking Application

## Project Overview

User Workspace is a simple web application designed to track visitor IP addresses and their geolocations using Express.js and an IP geolocation service. The application serves a static tracking page and responds to various requests to record and retrieve visitor data related to their IP addresses and locations.

## Installation

To install and run this application, you need to have [Node.js](https://nodejs.org/) installed on your machine. Follow the steps below to set up the project:

1. Clone the repository:
   ```bash
   git clone <REPOSITORY_URL>
   ```
2. Navigate to the project directory:
   ```bash
   cd user-workspace
   ```
3. Install the dependencies:
   ```bash
   npm install
   ```

## Usage

To start the server, run the following command:

```bash
node server.js
```

The server will be running at [http://localhost:8000](http://localhost:8000). You can access the tracking page by navigating to:

```
http://localhost:8000/trackpage
```

### Endpoints

- **GET /track:** Tracks a visitor's IP address and redirects them to a tracking URL.
- **GET /ips:** Returns a JSON array of all recorded visitor IP addresses.
- **POST /location:** Accepts location data in JSON format and records it.
  - Request body must include:
    ```json
    {
      "latitude": <number>,
      "longitude": <number>
    }
    ```
- **GET /locations:** Returns a JSON array of all recorded visitor locations.

## Features

- Tracks and logs visitor IP addresses.
- Uses geolocation service to ascertain and log the geographic coordinates of the IP addresses.
- Returns easily consumable JSON endpoints for integrated applications.
- Static serving of a tracking page prompting users for geolocation access.

## Dependencies

The project relies on the following Node.js packages, as defined in `package.json`:

- **express**: A minimal and flexible Node.js web application framework.
- **geolocation**: A library for obtaining the geographic location of IP addresses.

You may find the above dependencies listed in `package.json`:

```json
{
  "dependencies": {
    "express": "^5.1.0",
    "geolocation": "^0.2.0"
  }
}
```

## Project Structure

```plaintext
user-workspace/
│
├── server.js                # Main server file
├── package.json             # Project metadata and dependencies
└── package-lock.json        # Exact version of dependencies
└── public/
    └── trackpage.html       # Static HTML page served for tracking
```

## License

This project is open-source and available under the MIT License. 

For any inquiries, please contact [Your Name](mailto:your@email.com).
```