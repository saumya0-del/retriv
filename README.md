

## 🔌 Requirements
```
python>=3.8
```

## 💾 Installation
```bash
pip install retriv
```

## 💡 Minimal Working Example

```python
# Note: SearchEngine is an alias for the SparseRetriever
from retriv import SearchEngine

collection = [
  {"id": "doc_1", "text": "Generals gathered in their masses"},
  {"id": "doc_2", "text": "Just like witches at black masses"},
  {"id": "doc_3", "text": "Evil minds that plot destruction"},
  {"id": "doc_4", "text": "Sorcerer of death's construction"},
]

se = SearchEngine("new-index").index(collection)

se.search("witches masses")
```
Output:
```json
[
  {
    "id": "doc_2",
    "text": "Just like witches at black masses",
    "score": 1.7536403
  },
  {
    "id": "doc_1",
    "text": "Generals gathered in their masses",
    "score": 0.6931472
  }
]
```

