# LLM.txt File Generator

A tool for creating `llm.txt` files from GitHub repositories and cookbooks. This project consolidates code from various sources into single text files that can be easily consumed by Large Language Models (LLMs) as context. Additionally, it includes a curated collection of LLM prompt templates for common development tasks.

## 🎯 What are llm.txt Files?

`llm.txt` files are consolidated text documents that contain code from GitHub repositories or programming cookbooks merged into a single, LLM-friendly format. These files serve as comprehensive context that can be provided to Large Language Models to help them understand entire codebases, frameworks, or collections of examples.

### Use Cases
- **Codebase Understanding**: Provide an entire repository's code to an LLM for analysis, questions, or modifications
- **Learning from Examples**: Consolidate cookbook examples for AI-assisted learning and implementation
- **Context for Development**: Give LLMs full context of a project structure and implementation patterns
- **Code Migration**: Help LLMs understand legacy codebases for modernization or migration tasks

### Example
The `prompts/agents/agno agent cookbook.txt` file is a 2.9MB consolidated file containing all Python files from the agno agent framework, making it easy to provide comprehensive context to LLMs about the framework.

## 📁 Repository Structure

```
├── prompts/
│   ├── code-generation/    # Code generation prompts
│   ├── code-review/       # Code review and refactoring prompts
│   ├── documentation/     # Documentation generation prompts
│   ├── debugging/         # Debugging and troubleshooting prompts
│   └── agents/           # AI agent instruction templates & llm.txt examples
├── templates/            # Reusable prompt templates
├── examples/            # Usage examples and demonstrations
└── README.md           # This file
```

## 🚀 Quick Start

### Using llm.txt Files

1. **Find or Create**: Locate existing llm.txt files in `prompts/agents/` or create your own by consolidating code from GitHub repositories or cookbooks
2. **Provide Context**: Upload or paste the llm.txt file content to your LLM as context
3. **Ask Questions**: Query the LLM about the codebase, request modifications, or seek explanations

### Using Prompt Templates

1. Browse the `prompts/` directory for the type of prompt you need
2. Copy the relevant template
3. Replace the placeholder variables (e.g., `{language}`, `{code}`, `{requirements}`)
4. Use with your preferred LLM or AI agent

## 📝 Available Prompt Categories

### LLM.txt Files
- **Agent Cookbooks**: Consolidated code from agent frameworks and examples
- **GitHub Codebases**: Complete repository code merged into single files
- Location: `prompts/agents/` (example: `agno agent cookbook.txt`)

### Code Generation
- **General Code Generation**: Create functions, classes, and modules
- **Unit Tests**: Generate comprehensive test suites
- Location: `prompts/code-generation/`

### Code Review
- **Comprehensive Review**: In-depth code analysis and feedback
- **Refactoring Suggestions**: Code improvement recommendations
- Location: `prompts/code-review/`

### Documentation
- **Code Documentation**: Generate technical documentation
- Location: `prompts/documentation/`

### Debugging
- **Debug Assistant**: Systematic problem analysis and resolution
- Location: `prompts/debugging/`

### AI Agents
- **IDE Assistant**: Integrated development environment helper
- **Pair Programming**: Collaborative coding partner
- Location: `prompts/agents/`

## 🔧 Usage Examples

### Using an llm.txt File with an LLM

**Scenario**: Understanding the agno agent framework

1. Locate the llm.txt file: `prompts/agents/agno agent cookbook.txt`
2. Upload or paste its contents to your LLM (GPT-4, Claude, etc.)
3. Ask questions like:
   - "Explain how the agent_os works"
   - "Show me how to create a custom agent"
   - "What database integrations are available?"
   - "Help me implement a Slack interface for my agent"

The LLM will have the entire codebase as context and can provide detailed, accurate answers.

### Using a Code Generation Prompt

1. Open `prompts/code-generation/general-code-generation.txt`
2. Replace placeholders with your specific requirements:
   - `{requirements}` → "Create a function that validates email addresses"
   - `{language}` → "Python"
   - `{context}` → "User registration system"
3. Send to your LLM

### Customizing Agent Instructions

1. Select an agent template from `prompts/agents/`
2. Modify the context variables for your project
3. Integrate into your IDE or agent system

## 📚 Template Variables

Common variables used across prompts:
- `{language}` - Programming language
- `{code}` - Code to analyze/modify
- `{requirements}` - Specific requirements
- `{context}` - Project or usage context
- `{error_details}` - Error messages or symptoms

See `templates/variables-guide.md` for a complete list.

## 🤝 Contributing

Contributions are welcome! Please:
1. **llm.txt Files**: Submit consolidated codebases from GitHub or cookbooks in text format
2. **Prompt Templates**: Follow the existing template structure with clear placeholder variables
3. Include clear placeholder variables and usage examples
4. Test prompts with different LLMs when possible

### Creating llm.txt Files
When contributing new llm.txt files:
- Clearly indicate the source repository or cookbook
- Include a table of contents if the file is large
- Use markdown formatting for readability
- Add file path references for better navigation

## 📄 License

Licensed under the Apache License 2.0. See [LICENSE](LICENSE) for details.

## 🔗 Integration

### For llm.txt Files
- **LLM Context**: Upload to GPT-4, Claude, Gemini, LLaMA for comprehensive codebase understanding
- **AI Coding Assistants**: Provide as context to GitHub Copilot Chat, Cursor, or other AI IDEs
- **Custom Applications**: Integrate into your own AI-powered tools that need codebase context
- **Learning & Documentation**: Use for code reviews, architecture discussions, or training

### For Prompt Templates
- **IDEs**: VS Code, IntelliJ, Sublime Text (with AI extensions)
- **AI Agents**: GitHub Copilot, Amazon CodeWhisperer, TabNine
- **LLMs**: GPT-4, Claude, Gemini, LLaMA, and others
- **Custom Tools**: Your own AI-powered development tools

Perfect for developers, teams, and organizations looking to enhance their AI-assisted development workflow with comprehensive codebase context and ready-to-use prompt templates.
