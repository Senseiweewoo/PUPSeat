# 🚌 PUPSeat: Ride Booking System Simulator

Welcome to **PUPSeat**, a feature-rich desktop Ride Booking Simulator designed with a modern GUI and interactive mapping. PUPSeat simulates booking a ride anywhere in the Philippines, calculating real-time distances, and visualizing the pick-up and drop-off path on an interactive map.

Whether you're taking a standard sedan to class or commuting in a UFO, PUPSeat has you covered!

---

## 🌟 Features

* **Interactive Map Visualization**: Integrated `TkinterMapView` to dynamically display the start and destination locations in the Philippines with path lines.
* **Geocoded Distance Calculation**: Uses `geopy` to convert text locations (e.g., "Manila", "Quezon City") to geographic coordinates and compute geodesic distances.
* **Quirky Vehicle Fleet**: Choose from standard transit options or fantasy-grade vehicles, each with its own base rates and per-kilometer rates:
  * 🐎 **Horse** (₱30 base, ₱5/km)
  * 🏍️ **Motorcycle** (₱40 base, ₱10/km)
  * 🚗 **Sedan** (₱50 base, ₱15/km)
  * 🚙 **SUV** (₱60 base, ₱20/km)
  * 🚐 **Van** (₱70 base, ₱30/km)
  * 🛻 **Monster Truck** (₱150 base, ₱60/km)
  * 🚁 **Helicopter** (₱1,000 base, ₱200/km)
  * 🍫 **Elevator of Willy Wonka** (₱3,000 base, ₱500/km)
  * 🧞‍♂️ **Magic Carpet** (₱5,000 base, ₱800/km)
  * 🌀 **Tardis** (₱8,000 base, ₱1,100/km)
  * 🐉 **Dragon** (₱50,000 base, ₱10,000/km)
  * 🛸 **UFO** (₱100,000 base, ₱25,000/km)
* **Booking State Management**: Track bookings through their lifecycle: **Active**, **Finished**, or **Cancelled**, color-coded directly in a clean table view.
* **Local Persistence**: Saves all booking transactions in a CSV file (`bookings.csv`) so your history is preserved.

---

## 🛠️ Tech Stack

* **GUI Framework**: [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter) for a modern, sleek widget styling.
* **Map Engine**: [TkinterMapView](https://github.com/TomSchimansky/TkinterMapView) for embedding open-source maps.
* **Geocoding & Math**: [Geopy](https://github.com/geopy/geopy) for address lookup and distance mathematics.
* **Database**: CSV-based storage.

---

## 🚀 Installation & Setup

Follow these simple steps to run PUPSeat locally on your machine:

### 1. Prerequisites
Ensure you have Python 3.7+ installed.

### 2. Clone the Repository
```bash
git clone https://github.com/Senseiweewoo/PUPSeat.git
cd PUPSeat
```

### 3. Install Dependencies
Install all the required Python libraries using pip:
```bash
pip install -r requirements.txt
```

### 4. Run the Application
Start the simulator:
```bash
python main.py
```

---

## 📂 Project Structure

```text
PUPSeat/
│
├── backend/
│   ├── booking.py      # Methods to load/save bookings to CSV
│   ├── distance.py     # Geopy integration for coordinates & geodesic distance
│   └── vehicle.py      # Vehicle classes (OOP base & subclasses) and factory
│
├── frontend/
│   ├── app.py          # CustomTkinter GUI layout, map handling, & events
│   └── app_logo.ico    # Desktop window icon
│
├── bookings.csv        # Local CSV file database for booking records
├── requirements.txt    # List of project library dependencies
├── main.py             # Entrypoint file to launch the application
└── README.md           # Project documentation (this file)
```
