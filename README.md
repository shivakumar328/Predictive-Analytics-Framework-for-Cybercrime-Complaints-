
# Predictive Analytics Framework for Proactive Cybercrime Intervention

![Cybersecurity Data Banner](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

An AI/ML-driven framework designed to forecast likely cash withdrawal locations from financial cybercrimes, enabling law enforcement agencies (LEAs) and financial institutions (FIs) to take timely and proactive intervention measures.

## 📜 Project Overview

### The Problem
The National Cybercrime Reporting Portal currently receives approximately **8,000 complaints daily**, a number that is rapidly increasing. This high volume overwhelms law enforcement and financial institutions, forcing them into a reactive posture where they act only after a crime has been successfully executed. This leads to delayed investigations and a lower probability of recovering stolen funds.

### Our Solution
This project shifts the paradigm from reactive to **proactive intervention**. By leveraging predictive analytics on historical cybercrime data, our framework forecasts potential cash withdrawal hotspots *in advance*. This provides LEAs with actionable intelligence to deploy resources strategically, alert local banks or ATMs in high-risk zones, and significantly improve the chances of preventing financial loss and apprehending criminals.

The framework is designed to integrate seamlessly with existing systems like the Citizen Financial Cyber Fraud Reporting and Management System, enhancing coordination between LEAs and FIs for faster fund blocking and recovery.

***

## ✨ Key Deliverables

This framework is built upon four core components:

* **🧠 a. Predictive Analytics Engine:** An AI/ML-based system that analyzes historical cybercrime and financial data to predict potential withdrawal hotspots. Its features include advanced pattern detection, geospatial risk modeling, and the ability to generate real-time alerts.

* **🗺️ b. Risk Heatmap Dashboard:** A GIS-enabled dashboard that visualizes real-time and potential risk zones across the country. It provides interactive, drill-down filters by time, location, crime category, and other relevant parameters.

* **🛡️ c. Law Enforcement Interface:** A secure, access-controlled web interface for investigators and officers. It provides direct access to alerts, detailed intelligence reports, case data, and evidence documentation to support field operations.

* **🚨 d. Alert & Notification System:** A robust, multi-channel notification system that pushes real-time alerts to designated law enforcement personnel, banks, and I4C officers via SMS, email, API triggers, or direct dashboard notifications.

***

## ⚙️ System Architecture

The framework operates on a multi-layered architecture designed for scalability, security, and real-time processing. Data flows from the National Cybercrime Reporting Portal, is processed by our predictive engine, and the resulting intelligence is disseminated through various user-facing components.



1.  **Data Ingestion:** Securely pulls anonymized, historical complaint data.
2.  **Preprocessing & Feature Engineering:** Cleans data and extracts relevant features, including geospatial attributes.
3.  **Predictive Modeling (AI/ML Core):** The engine runs trained models (e.g., Gradient Boosting, LSTMs) to generate risk scores and predict hotspot locations.
4.  **Intelligence Storage:** Predictions and alerts are stored in a secure, high-performance database (e.g., PostgreSQL with PostGIS).
5.  **Dissemination Layer:** An API serves the processed intelligence to the Heatmap Dashboard, LEA Interface, and the Alerting System.

***

## 💻 Tech Stack

* **Backend & Machine Learning:** Python, Pandas, GeoPandas, Scikit-learn, TensorFlow/Keras
* **Database:** PostgreSQL with PostGIS extension for geospatial queries
* **API:** FastAPI / Django Rest Framework
* **Frontend & Dashboard:** React.js, Deck.gl, Mapbox / Leaflet.js
* **Alerting:** Twilio (for SMS), SendGrid (for Email), Celery & Redis (for asynchronous tasks)

***

## 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites
* Python 3.9+
* Node.js and npm
* PostgreSQL with PostGIS extension

### Installation

1.  **Clone the repo:**
    ```sh
    git clone [https://github.com/shivakumar328/Cybercrime-Hotspot-Prediction.git](https://github.com/shivakumar328/Cybercrime-Hotspot-Prediction.git)
    cd Cybercrime-Hotspot-Prediction
    ```

2.  **Setup Backend:**
    ```sh
    cd backend
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    pip install -r requirements.txt
    ```

3.  **Setup Frontend:**
    ```sh
    cd frontend
    npm install
    ```

4.  **Configure Environment Variables:**
    * Create a `.env` file in the `backend` directory and add your database credentials, API keys, etc.

***

## 📖 Usage

1.  **Run the Backend Server:**
    ```sh
    cd backend
    uvicorn main:app --reload
    ```

2.  **Launch the Frontend Dashboard:**
    ```sh
    cd frontend
    npm start
    ```

3.  **Train the Predictive Model:**
    * Place your dataset in the `/data` folder.
    * Execute the training script:
        ```sh
        python scripts/train_model.py
        ```

***

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

***

## 📄 License

Distributed under the MIT License. See `LICENSE.txt` for more information.
