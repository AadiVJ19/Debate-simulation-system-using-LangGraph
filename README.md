# Debate-simulation-system-using-LangGraph
# AI Debate Simulation System

A LangGraph-based debate simulation system where two AI agents engage in a structured argument over a fixed topic.

## Features

- Two AI agents (Scientist vs Philosopher) debate in alternating turns
- 8-round debate structure (4 arguments per agent)
- Memory system that preserves debate history
- Automated judging system that determines a winner
- CLI interface for topic input
- Comprehensive logging of debates

## Requirements

- Python 3.8+
- LangGraph >= 0.1.0
- Google Generative AI API key

## Installation


1. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
2. Set up environment variables:
   - Create a `.env` file in the project root
   - Add your Google API key:
     ```
     GOOGLE_API_KEY=your_api_key_here (check GOOGLE AI STUDIOS for API key and make sure to not share it with anyone and keep it private).
     ```

## Usage

1. Run the main script:
   ```
   python main.py
   ```
2. Enter your debate topic when prompted
3. Watch the debate unfold between Scientist and Philosopher
4. View the final judgment and debate summary

## Project Structure

- `main.py`: Main execution script
- `nodes.py`: Contains all node implementations (UserInputNode, AgentNode, MemoryNode, JudgeNode)
- `requirements.txt`: Project dependencies
- `README.md`: Documentation

## Output

The system generates:
- Real-time CLI output of the debate
- Log files containing complete debate transcripts
- Final judgment with winner and reasoning

## DAG Structure

The system uses a directed acyclic graph (DAG) with the following nodes:

```
UserInputNode -> AgentA -> Memory -> AgentB -> Memory -> JudgeNode
```
refer to image provided
'''

Each node handles specific aspects of the debate:
- UserInputNode: Accepts debate topic
- AgentNodes: Generate arguments based on personas
- MemoryNode: Maintains debate history
- JudgeNode: Evaluates debate and declares winner

