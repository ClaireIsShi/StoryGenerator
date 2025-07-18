# Story Generator

Hi there guys! This is an auto Story Generator using OpenAI and Anthropic's LLMs (of course you can use different LLMs by changing settings in  `settings.py`).

You can use this to generate a story from a given topic and instruction. See if you can generate a funny story with your own prompts!

You don't need a strong prompt to generate a story———all prompts and arguments are already prepared for you. If you're not familiar with running code in the shell, you can use  `test.ipynb` notebook to execute the program. Alternatively, follow the steps below.


You'll notice a `result.json` file in this directory. This is just an example to show you where the final output will be saved. You can delete this file and generate your own story.

Note that the bash example below doesn't include all possible arguments. If you want to modify other parameters, please edit the `settings.py` file.

## 1 environment setup
Python 3.10 is a good choice for this project, because this is the version I use.

## 2 install packages
```bash
pip install -r requirements.txt
```
## 3 run in bash
After install all required packages, you can run 
```bash
python main.py --OPENAI_API_KEY your_key --ANTHROPIC_API_KEY your_key\
--MAIN_CHARACTOR your_own_character --TOPIC your_story_topic --MAIN_GOAL your_character_main_goal --LANGUAGE your_language
```
or just run
```bash
python main.py --OPENAI_API_KEY your_key --ANTHROPIC_API_KEY your_key
```
For a sample example, an English love-fiction.
