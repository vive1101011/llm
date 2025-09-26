# Example: TypeScript API Endpoint

## Prompt
You are an expert software developer. Generate clean, efficient, and well-documented code based on the following requirements:

Requirements: Create a REST API endpoint that handles user authentication with JWT tokens
Programming Language: TypeScript
Context: Express.js backend application with MongoDB database

Please provide:
1. Clean, readable code that follows best practices
2. Appropriate comments explaining complex logic
3. Error handling where necessary
4. Brief explanation of the approach

## Expected Response
```typescript
import { Request, Response, NextFunction } from 'express';
import jwt from 'jsonwebtoken';
import bcrypt from 'bcrypt';
import { User } from '../models/User';

interface LoginRequest extends Request {
  body: {
    email: string;
    password: string;
  };
}

interface AuthResponse {
  success: boolean;
  message: string;
  token?: string;
  user?: {
    id: string;
    email: string;
    name: string;
  };
}

/**
 * Authenticates a user and returns a JWT token
 * POST /api/auth/login
 */
export const loginUser = async (
  req: LoginRequest,
  res: Response<AuthResponse>,
  next: NextFunction
): Promise<void> => {
  try {
    const { email, password } = req.body;

    // Input validation
    if (!email || !password) {
      res.status(400).json({
        success: false,
        message: 'Email and password are required'
      });
      return;
    }

    // Find user by email
    const user = await User.findOne({ email: email.toLowerCase() });
    if (!user) {
      res.status(401).json({
        success: false,
        message: 'Invalid credentials'
      });
      return;
    }

    // Verify password
    const isValidPassword = await bcrypt.compare(password, user.hashedPassword);
    if (!isValidPassword) {
      res.status(401).json({
        success: false,
        message: 'Invalid credentials'
      });
      return;
    }

    // Generate JWT token
    const token = jwt.sign(
      { 
        userId: user._id, 
        email: user.email 
      },
      process.env.JWT_SECRET as string,
      { 
        expiresIn: '24h',
        issuer: 'your-app-name'
      }
    );

    // Return success response
    res.status(200).json({
      success: true,
      message: 'Authentication successful',
      token,
      user: {
        id: user._id.toString(),
        email: user.email,
        name: user.name
      }
    });

  } catch (error) {
    console.error('Login error:', error);
    res.status(500).json({
      success: false,
      message: 'Internal server error'
    });
  }
};
```

## Explanation
This TypeScript function implements a secure user authentication endpoint with the following features:

1. **Type Safety**: Uses TypeScript interfaces for request/response typing
2. **Security**: Implements bcrypt for password comparison and JWT for token generation
3. **Error Handling**: Comprehensive error handling with appropriate HTTP status codes
4. **Input Validation**: Checks for required fields before processing
5. **Security Best Practices**: 
   - Doesn't expose sensitive information in error messages
   - Uses environment variables for JWT secret
   - Implements proper token expiration
   - Normalizes email to lowercase for consistency

The function follows REST API conventions and provides clear feedback to clients while maintaining security.