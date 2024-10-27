# Self-Learning Text Generation Agent using DSP
A Python-based AI agent that leverages DSPy to improve its response quality iteratively by using self-feedback loops. The agent generates responses, evaluates them using a stronger model, and adjusts based on feedback, ultimately enhancing the precision and clarity of its answers over time.

## Features:
**Self-Feedback Mechanism:**
Automatically evaluates initial responses and iterates to produce improved answers.

**Adaptive Learning with DSPy:**
Continuously refines response accuracy by incorporating feedback into its internal model.

**Modular and Extensible:** 
The agent structure allows easy updates, enabling it to support additional models or custom domain knowledge.

## Project Structure
```markdown
self-learning-agent/
│
├── agent.py         # Main agent logic
├── feedback.py      # Logic for feedback mechanism
├── templates.py     # Contains initial prompt templates
└── requirements.txt # Required dependencies
```

## Prerequisites:
Python 3.8+

DSPy: Install via ```pip install dspy```.

OpenAI API Key: Sign up on OpenAI to get an API key for GPT models.

Aetting Started
Clone the Repository

```
git clone https://github.com/yourusername/self-learning-agent.git
cd self-learning-agent
```
### Install Dependencies
Install the required libraries using ```pip```:
```
pip install -r requirements.txt
```
### Add Your OpenAI API Key
Replace ```'your-openai-api-key'``` in agent.py with your actual ```OpenAI API key```.

### Usage
To start the agent, run the ```agent.py``` file:

```
python agent.py
```
### Example Interaction
The agent will prompt you to enter a question. 
For example:

```
Enter your question: What is the capital of France?
```
Output:
```
Initial response: Paris is the capital of France.
Score: 9

Improved response: Paris is the capital of France, and it is known for its rich history and culture.
Improved Score: 10
```
## Expected Workflow
**Initial Query:** The agent takes a user input query.

**Response Generation:** Generates an initial response using a less powerful model (e.g., GPT-3.5-turbo).

**Evaluation:** Evaluates the response using a more advanced model (e.g., GPT-4) to assign a score between 0 and 10.

**Feedback Loop:** Adjusts the response based on feedback, aiming for a higher-quality answer.

**Self-Improvement:** DSPy enables the agent to update its internal structure based on feedback, making it smarter with each cycle.
## Code Explanation
### `agent.py`
This file contains the main class SelfLearningAgent, which handles response generation, evaluation, and improvement cycles.

### `feedback.py`
Implements the evaluation mechanism, using a stronger LLM model to assess the correctness and clarity of responses.

### `templates.py`
Defines the basic prompt templates for generating responses.

## Contributing
We welcome contributions! Please feel free to submit issues, feature requests, or pull requests.

## License
This project is licensed under the MIT License.

