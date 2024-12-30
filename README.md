# EventSync

A MicroSaaS for simple local event management, communication, and venue coordination.

## Features
- **Smart Scheduling**: Avoid conflicts with local calendars.
- **RSVP & Updates**: Manage RSVPs and send notifications.
- **Venue Suggestions**: Recommend venues based on needs.

## Setup
1. Clone:
   ```bash
   git clone https://github.com/yourusername/EventSync.git && cd EventSync
   ```
2. Install:
   ```bash
   pip install -r requirements.txt
   ```
3. Configure:
   ```bash
   cp .env.example .env  # Add keys in .env
   ```
4. Run:
   ```bash
   python app.py
   ```

## Implementation
Python Flask app:

```python
from flask import Flask, request, jsonify

app = Flask(__name__)

@app.route('/create_event', methods=['POST'])
def create_event():
    return jsonify({"message": "Event created"}), 201

@app.route('/rsvp', methods=['POST'])
def rsvp():
    return jsonify({"message": "RSVP received"}), 200

if __name__ == '__main__':
    app.run(debug=True)
```
