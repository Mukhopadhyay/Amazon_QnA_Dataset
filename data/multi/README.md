# Multi answer dataset
The questions present in this directory contains more than one answer. Which is why they're seperated into different subdirectories. Please use `QuestionID` attribute to join the `multi_questions` and `multi_answers` datasets

---

## Starter Code (Reading the data as `pd.DataFrame`)

### Answers dataset
```python
import os
import pandas as pd

answers_path = 'data/multi/answers'
answers = pd.concat(
    [
        pd.read_csv(
            os.path.join(answers_path, fname)
        ) for fname in os.listdir(answers_path) if fname.endswith('.csv')
    ]
)
```

---

### Questions dataset
```python
import os
import pandas as pd

questions_path = 'data/multi/questions'
questions = pd.concat(
    [
        pd.read_csv(
            os.path.join(questions_path, fname)
        ) for fname in os.listdir(questions_path) if fname.endswith('.csv')
    ]
)
```

---

### Available Categories
* Automotive
* Baby
* Beauty
* Cell Phones and Accessories
* Clothing Shoes and Jewelry
* Electronics
* Grocery and Gourmet Food
* Health and Personal Care
* Home and Kitchen
* Musical Instruments
* Office Products
* Patio Lawn and Garden
* Pet Supplies
* Sports and Outdoors
* Tools and Home Improvement
* Toys and Games
* Video Games

---

### Multi-Question dataset info
|Category|# Questions|# Answers|
|:-------|:----------|:--------|
|Automotive|10577|233784|
|Baby|3754|82034|
|Beauty|5857|125652|
|Cell Phones and Accessories|10320|237220|
|Clothing Shoes and Jewelry|2871|66709|
|Electronics|38959|867921|
|Grocery and Gourmet Food|2997|62243|
|Health and Personal Care|10766|255209|
|Home and Kitchen|24329|611335|
|Musical Instruments|2976|67326|
|Office Products|5634|130088|
|Patio Lawn and Garden|7909|193780|
|Pet Supplies|4731|133274|
|Sports and Outdoors|19102|444900|
|Tools and Home Improvement|13315|327597|
|Toys and Games|7337|151779|
|Video Games|1183|28893|
|**Total**|**172617**|**4019744**|
---