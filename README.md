# Korean Task-oriented Dialogue (ToD) Dataset in the Insurance Domain

## Korean ToD dataset
We utilized a generative model to compile a high-quality dataset of Korean-language dialogue content about insurance services, and we are making it publicly available for further research.

## Data schema
```json
  "dialogue_data": [
    {
      "scenario_id": "Scenario_ID",
      "domain": "Scenario_Domain",
      "scenario_type": "Scenario_Type",
      "dialogue_turns": [
        {
          "turn_number": "Turn_Number",
          "speaker": "Speaker",
          "utterance": "Utterance",
          "act": "Act",
          "slots": [
            {
              "slot_type": "Slot_Type",
              "slot_values": "Slot_Values"
            }
          ]
        }
      ]
    }
  ]
```

## Usage

### Load json file

```python
>>> import json
>>> with open('korean_dialogue_data.json', 'r') as json_file:
    loaded_data = json.load(json_file)
```

### Data example

```python
>>> print(loaded_data[0]["data"][1])
{'turn': 1, 'speaker': 'System', 'utterance': '안녕하세요. 70세 이상 분들도 가입 가능한 보험이 있는지 궁금합니다.', 'act': 'INFORM_INTENT', 'slot': [{'slot_type': 'AGE', 'values': '70세'}]}
```
