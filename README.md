# Story Generator

Hi there guys! This is an auto Story Generator using OpenAI and Anthropic's LLMs (of course you can use different LLMs by changing settings in  `settings.py`).

You can use this to generate a story from a given topic and instruction. See if you can generate a funny story with your own prompts!

# Structure
```
StoryGenerator
├── End
│   ├── EndsGenerate.py          # Python script responsible for generating the ending of the story. It may invoke LLMs to produce a conclusion that meets the requirements.
│   ├── __init__.py              # Python package initialization file that makes the End directory an importable package.
│   └── build.py                 # Builds the graph structure or modules related to story ending generation, possibly for resource integration.
├── Expender
│   ├── ExpenderWriterSimulator.py # Implements the core logic for story expansion. It invokes LLMs to generate expanded stories, handles retry logic, and updates outlines.
│   ├── Interact.py              # Handles the interaction logic during the story expansion process, which may include user input processing and feedback mechanisms.
│   ├── ReaderSimulator.py       # Simulates readers to evaluate the story and provides feedback on logical and character growth issues.
│   ├── __init__.py              # Python package initialization file that makes the Expender directory an importable package.
│   └── build.py                 # Builds the graph structure or components of the story expansion module to organize the expansion process.
├── Memory
│   ├── MemoryStore.py           # Manages the memory storage of the story, which may be used to store historical stories, outlines, and other information.
│   └── __init__.py              # Python package initialization file that makes the Memory directory an importable package.
├── PlainGenerator
│   ├── PlainGenerate.py         # Python script for generating standard story paragraphs. It invokes LLMs to produce paragraphs that meet the specifications.
│   ├── PlainWritingAssistant.py # Assists in generating standard story paragraphs by providing writing suggestions or templates.
│   └── __init__.py              # Python package initialization file that makes the PlainGenerator directory an importable package.
├── StoryStarter
│   ├── StoryStartGenerate.py    # Python script responsible for generating the beginning of the story, determining the starting plot.
│   └── __init__.py              # Python package initialization file that makes the StoryStarter directory an importable package.
├── TwistGenerator
│   ├── TwistGenerate.py         # Python script for generating plot twists in the story, adding dramatic elements.
│   └── __init__.py              # Python package initialization file that makes the TwistGenerator directory an importable package.
├── MainGraph.py                 # Builds the main graph structure for story generation, integrating various sub - modules (such as beginning, expansion, twist, ending, etc.).
├── StoryState.py                # Defines the data structure of the story state, using TypedDict or other methods to standardize state information.
├── main.py                      # The main entry point of the project. It parses command - line arguments and invokes the main graph to start the story generation process.
├── README.md                    # Project documentation that introduces the project's functionality, environment setup steps, running commands, etc.
├── requirements.txt             # Lists the Python dependencies and their versions required for the project to run.
├── settings.py                  # Project configuration file containing LLM API configurations, path settings, default parameter values, etc.
├── test.ipynb                   # Jupyter Notebook file that provides project running examples and test code for users to quickly get started.
└── utils.py                     # Utility function file containing environment variable settings, text processing, helper functions, etc.
```
You don't need a strong prompt to generate a story———all prompts and arguments are already prepared for you. If you're not familiar with running code in the shell, you can use  `test.ipynb` notebook to execute the program. Alternatively, follow the steps below.


You'll notice a `result.json` file in this directory. This is just an example to show you where the final output will be saved. You can delete this file and generate your own story.

Note that the bash example below doesn't include all possible arguments. If you want to modify other parameters, please edit the `settings.py` file.
# How to run this project?
## 1 environment setup
Python 3.10 is a good choice for this project, because this is the version I use.

## 2 install packages
```
pip install -r requirements.txt
```
## 3 run in bash
After install all required packages, you can run 
```
python main.py --OPENAI_API_KEY your_key --ANTHROPIC_API_KEY your_key\
--MAIN_CHARACTOR your_own_character --TOPIC your_story_topic --MAIN_GOAL your_character_main_goal --LANGUAGE your_language
```
or just run
```
python main.py --OPENAI_API_KEY your_key --ANTHROPIC_API_KEY your_key
```
For a sample example, an English love-fiction.
