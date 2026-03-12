"# NexaThon" 
from flask import Flask, request, jsonify

app = Flask(__name__)

# Sample hospital data
hospitals = [
    {"name": "RIMS", "location": "Bariatu"},
    {"name": "Sadar Hospital", "location": "Namkum"},
    {"name": "Paras HEC Hospital", "location": "Dhurwa"},
    {"name": "Orchid Hospital", "location": "Lalpur"},
    {"name": "Aalam Hospital", "location": "Bariatu"}
]

# Donor database (temporary)
donors = []

# -------- Find Hospital --------
@app.route('/find_hospital', methods=['GET'])
def find_hospital():
    location = request.args.get('location')

    result = [h for h in hospitals if h["location"].lower() == location.lower()]

    return jsonify(result)


# -------- Register Donor --------
@app.route('/register_donor', methods=['POST'])
def register_donor():
    data = request.json

    donor = {
        "name": data["name"],
        "blood": data["blood"],
        "phone": data["phone"],
        "location": data["location"]
    }

    donors.append(donor)

    return jsonify({"message": "Donor Registered Successfully"})


# -------- Find Donor --------
@app.route('/find_donor', methods=['GET'])
def find_donor():
    blood = request.args.get('blood')

    result = [d for d in donors if d["blood"] == blood]

    return jsonify(result)


# -------- Run Server --------
if __name__ == '__main__':
    app.run(debug=True)
