# Story Generator

Hi there guys! This is n auto Story Generator using Openai and Anthropic's LLMs.(of course you can use different LLMs by changing settings in `settings.py`).


You can use this to generate a story from a given topic and a given instruction, see if you can generate a funny story with your instruction and topic:)


You don't need strong prompt to generate story, all prompts and args are already prepared for you.
If you're not familiar with running code in shell, you can use `test.py` to run the code. Or, following these steps below.

You could see we put a `result.json` file under this document, this's just a file example to show you where the final output goes to. You can delete this file anyway and generate your own story there.

Just for instance, we didn't put many args in bash example below. If you want to change any other params, please go to `setting.py` file to edit them.

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
