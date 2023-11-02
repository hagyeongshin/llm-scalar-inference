# batch-write-prompt

In psycholinguistic experiments and when evaluating LLMs à la Marvin & Linzen (2018), items/prompts vary only for the targeted linguistic phenomenon (e.g., subject-verb agreement). This notebook demonstrates how to batch-write those prompts/items more efficiently using built-in Python functions.

This notebook recreates items from Bott & Noveck (2004). In their study, six different sentence types (listed below) were created with "categories" and "exemplars," expressing semantically or pragmatically true or false statements. The categories used in the study were 'fish,' 'reptile,' 'bird,' 'mammal,' 'insect,' and 'shellfish.' Exemplars included 'anchovies,' 'alligator,' 'eagle,' 'cat,' 'wasp,' and 'winkle.' This notebook generates dictionaries that include entries for text types (i.e., experimental conditions) and prompts/items. See below for examples.

Sentence types from Bott & Noveck (2004): \
T1 = 'Some {E} are {C}.'\
T2 = 'Some {C} are {E}.'\
T3 = 'Some {E} are {WC}.'\
T4 = 'All {E} are {C}.'\
T5 = 'All {C} are {E}.'\
T6 = 'All {E} are {WC}.'

This notebook writes a list of dictionaries in the format of:\
[{'type': 'TI', 'sentence': 'Some cats are mammals.'}\
{'type': 'T2', 'sentence': 'Some mammals are cats.'}\
{'type': 'T3', 'sentence': 'Some cats are fish.'}\
{'type': 'T4', 'sentence': 'All cats are mammals.'}\
{'type': 'T5', 'sentence': 'All mammals are cats.'}\
{'type': 'T6', 'sentence': 'All cats are fish.'}...]
