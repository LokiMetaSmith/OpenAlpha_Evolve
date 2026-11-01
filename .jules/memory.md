## Archived: 2026-10-31

### Repository Context
* **OpenAlpha_Evolve**: An open-source Python framework inspired by DeepMind's AlphaEvolve.
* **Purpose**: An intelligent system that iteratively writes, tests, and improves code using Large Language Models (LLMs) via LiteLLM, guided by evolutionary principles.
* **Architecture**: Modular, agent-based architecture including:
  * `TaskManagerAgent`: Orchestrates the evolutionary loop.
  * `PromptDesignerAgent`: Crafts prompts for the LLM (initial, mutation, bug-fix).
  * `CodeGeneratorAgent`: Generates Python code using LLMs (currently configured for Gemini).
  * `EvaluatorAgent`: Checks syntax, executes code in a sandboxed Docker environment, and scores fitness.
  * `DatabaseAgent`: Stores programs, fitness scores, generation, and lineage (in-memory).
  * `SelectionControllerAgent`: Selects parents for offspring and survivors for the next generation.
* **Configuration**: Managed via `config/settings.py` and `.env` for system parameters and API keys.
* **Task Definition**: Users define tasks using YAML files (recommended) or Python code. Examples include inputs, expected outputs, and constraints.
* **Execution Flow**: Driven by `main.py`, which loads a YAML configuration, initializes the `TaskManagerAgent`, and executes the evolutionary process.

### Active Session Memories
* Listed root directory contents using `ls -la`.
* Read `README.md` to understand the project vision, structure, and usage.
* Viewed the content of `main.py` to trace the execution flow and configuration loading.
* Wrote and executed an initial `archive.py` script to explore creating a memory archiving solution.
* Listed directories two levels deep using `tree -L 2`.
* Read `core/interfaces.py` to examine the core data structures (`Program`, `TaskDefinition`) and agent interfaces.
