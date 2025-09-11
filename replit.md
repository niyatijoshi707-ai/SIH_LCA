# Overview

LCA.AI is a web application for metallurgy and mining assessment that uses Google's Gemini AI to analyze uploaded images containing metals. The application identifies metals in images and provides detailed information about their recyclability and reuse potential. Built with Flask as a lightweight web framework, the application serves as an environmental assessment tool for metal waste management and circular economy initiatives.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Web Framework
The application uses Flask as the primary web framework, chosen for its simplicity and rapid development capabilities. This lightweight approach is suitable for the focused scope of image analysis and AI integration without the overhead of more complex frameworks.

## Frontend Architecture
The frontend consists of simple HTML templates with embedded CSS, following a minimalist approach. The application uses server-side rendering through Flask's Jinja2 templating engine, eliminating the need for complex client-side JavaScript frameworks. This architecture prioritizes simplicity and quick load times over dynamic interactivity.

## AI Integration
Google's Gemini 2.0 Flash model handles the core image analysis functionality. The integration uses the google.generativeai library to send images directly to the AI service for metal detection and recyclability assessment. This cloud-based approach eliminates the need for local machine learning infrastructure while providing access to state-of-the-art vision capabilities.

## File Management
Images are stored locally in an "uploads" directory structure, with the PIL (Python Imaging Library) handling image processing before sending to the AI service. This temporary storage approach keeps the application stateless while ensuring proper image format handling.

## Configuration Management
Environment variables manage sensitive configuration like API keys, following security best practices by keeping credentials out of the codebase. The application defaults to placeholder values for development while expecting production values from the environment.

# External Dependencies

## AI Services
- **Google Gemini API**: Core image analysis service requiring API key authentication
- **google.generativeai**: Python client library for Gemini integration

## Image Processing
- **PIL (Pillow)**: Image manipulation and format handling library

## Web Framework
- **Flask**: Lightweight web application framework for Python

## Environment Requirements
- **Python runtime environment**
- **GEMINI_API_KEY environment variable**: Required for AI service authentication

## File System
- **Local file storage**: Temporary image upload storage in "uploads" directory
- **Static file serving**: CSS and potential static assets served through Flask