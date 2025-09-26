# LLM Text Collection

A curated collection of LLM prompt templates and instructions for IDEs and AI agents. This repository provides ready-to-use text prompts for common development tasks including code generation, code review, documentation, debugging, and agent interactions.

## 📁 Repository Structure

```
├── prompts/
│   ├── code-generation/    # Code generation prompts
│   ├── code-review/       # Code review and refactoring prompts
│   ├── documentation/     # Documentation generation prompts
│   ├── debugging/         # Debugging and troubleshooting prompts
│   └── agents/           # AI agent instruction templates
├── templates/            # Reusable prompt templates
├── examples/            # Usage examples and demonstrations
└── README.md           # This file
```

## 🚀 Quick Start

1. Browse the `prompts/` directory for the type of prompt you need
2. Copy the relevant template
3. Replace the placeholder variables (e.g., `{language}`, `{code}`, `{requirements}`)
4. Use with your preferred LLM or AI agent

## 📝 Available Prompt Categories

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
1. Follow the existing template structure
2. Include clear placeholder variables
3. Provide usage examples
4. Test prompts with different LLMs when possible

## 📄 License

Licensed under the Apache License 2.0. See [LICENSE](LICENSE) for details.

## 🔗 Integration

These prompts work with:
- **IDEs**: VS Code, IntelliJ, Sublime Text (with AI extensions)
- **AI Agents**: GitHub Copilot, Amazon CodeWhisperer, TabNine
- **LLMs**: GPT-4, Claude, Gemini, LLaMA, and others
- **Custom Tools**: Your own AI-powered development tools

Perfect for developers, teams, and organizations looking to enhance their AI-assisted development workflow.
