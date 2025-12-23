from flask import Flask, request, jsonify

app = Flask(__name__)

data = {}

@app.route('/set', methods=['POST'])
def set_value():
    body = request.json
    data[body['key']] = body['value']
    return {"status": "saved"}

@app.route('/get/<key>', methods=['GET'])
def get_value(key):
    if key in data:
        return {"value": data[key]}
    return {"error": "not found"}, 404

app.run(host="0.0.0.0", port=5000)
