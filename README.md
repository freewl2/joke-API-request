import requests
import json
from pprint import pprint

url = "https://icanhazdadjoke.com"

payload={}
headers = {
  'Accept': 'application/json'
}

response = requests.request("GET", url, headers=headers, data=payload)

responseJson = response.json()

print("My generated joke is: " + str(responseJson['joke']))
