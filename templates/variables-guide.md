## Prompt Template Variables

This document explains common variables used in the LLM prompt templates.

### Code Generation Variables
- `{requirements}` - Detailed requirements for the code to generate
- `{language}` - Programming language (Python, JavaScript, Java, etc.)
- `{context}` - Additional context about the project or use case
- `{code_placeholder}` - Where the generated code will be placed
- `{explanation_placeholder}` - Where the explanation will be provided

### Code Review Variables
- `{code}` - The code to be reviewed
- `{language}` - Programming language of the code
- `{context}` - Project context or specific focus areas
- `{summary}` - Brief overview of findings
- `{issues}` - Specific issues identified
- `{suggestions}` - Recommendations for improvement
- `{rating}` - Numerical rating (1-10)

### Documentation Variables
- `{project_context}` - Information about the project
- `{audience}` - Target audience (developers, end-users, etc.)
- `{format}` - Documentation format (Markdown, JSDoc, etc.)

### Debugging Variables
- `{problem_description}` - Description of the issue
- `{error_details}` - Error messages, stack traces, etc.
- `{frameworks}` - Libraries and frameworks in use
- `{os}` - Operating system information
- `{additional_context}` - Any other relevant information

### Agent Variables
- `{project_name}` - Name of the current project
- `{primary_language}` - Main programming language
- `{current_file}` - File currently being worked on
- `{user_experience}` - User's experience level (beginner, intermediate, expert)
- `{current_task}` - Description of current task
- `{tech_stack}` - Technologies being used
- `{timeline}` - Project timeline or deadlines
- `{constraints}` - Any limitations or constraints