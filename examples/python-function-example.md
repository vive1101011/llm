# Example: Python Function Generation

## Prompt
You are an expert software developer. Generate clean, efficient, and well-documented code based on the following requirements:

Requirements: Create a function that validates email addresses using regex
Programming Language: Python
Context: This function will be used in a user registration system

Please provide:
1. Clean, readable code that follows best practices
2. Appropriate comments explaining complex logic
3. Error handling where necessary
4. Brief explanation of the approach

## Expected Response
```python
import re
from typing import bool

def validate_email(email: str) -> bool:
    """
    Validates an email address using regex pattern matching.
    
    Args:
        email (str): Email address to validate
        
    Returns:
        bool: True if email is valid, False otherwise
        
    Raises:
        TypeError: If email is not a string
    """
    if not isinstance(email, str):
        raise TypeError("Email must be a string")
    
    # Regex pattern for basic email validation
    # Matches: username@domain.tld format
    pattern = r'^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$'
    
    return bool(re.match(pattern, email))
```

Explanation:
This function uses a regex pattern to validate email addresses. It includes type hints for better code documentation, handles the case where a non-string is passed, and uses a comprehensive regex pattern that covers most valid email formats. The pattern ensures there's a username part, an @ symbol, a domain, and a valid top-level domain.