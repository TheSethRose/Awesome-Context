# Awesome Context

🚀 **A comprehensive collection of curated technology stack configurations and code examples for AI-powered development assistance.**

## Overview

Awesome Context provides structured YAML configuration files containing carefully curated code examples, best practices, and implementation patterns for dozens of popular technology stacks. These configurations are designed to provide rich context to AI coding assistants, enabling more accurate and helpful code generation.

## Features

- 📚 **50+ Technology Stacks** - From web frameworks to databases, ML libraries to cloud platforms
- 🎯 **Curated Examples** - Hand-picked, real-world code snippets and patterns
- 🔧 **Structured Format** - Consistent YAML schema for easy parsing and integration
- 🤖 **AI-Optimized** - Formatted specifically for optimal AI assistant performance
- 🌐 **Open Source** - Community-driven with contributions welcome

## Technology Stacks Included

### Web Frameworks

- React, Vue, Angular, Svelte
- Next.js, Express, FastAPI, Django
- Flask, Laravel, Rails, Spring Boot

### Databases & Storage

- PostgreSQL, MongoDB, Redis
- Elasticsearch, Qdrant (Vector DB)

### Cloud & DevOps

- Docker, Kubernetes, Compose
- AWS, Azure, GCP patterns

### Programming Languages

- JavaScript/TypeScript, Python, Go
- Java, Rust, C++, Swift, Kotlin

### AI & Machine Learning

- PyTorch, TensorFlow, Scikit-learn
- LangChain, Hugging Face Transformers
- OpenRouter API examples

### Additional Tools

- CSS Frameworks (Tailwind, Bootstrap)
- Testing (Jest, Pytest)
- Build Tools & Development workflows

## Quick Start Guide

### Using with AI Assistants

Each YAML file contains structured examples that can be loaded into AI coding assistants to provide relevant context for your projects.

```yaml
# Example structure from react.yaml
name: "React"
description: "A JavaScript library for building user interfaces"
categories: ["frontend", "javascript", "ui"]
examples:
  - title: "Functional Component with Hooks"
    code: |
      import React, { useState, useEffect } from 'react';

      function MyComponent() {
        const [data, setData] = useState(null);
        // ... rest of example
      }
```

### Integration Steps

1. **Clone the repository:**

   ```bash
   git clone https://github.com/TheSethRose/Awesome-Context.git
   cd Awesome-Context
   ```

2. **Use with your AI assistant:**

   - Load relevant YAML files as context
   - Reference specific examples for your technology stack
   - Use patterns as starting points for your implementations

## Configuration Schema

Each technology stack follows a consistent schema:

```yaml
name: string              # Technology name
description: string       # Brief description
version: string           # Version or latest
categories: [string]      # Categories (frontend, backend, database, etc.)
documentation_url: string # Official documentation link
examples:                 # Array of code examples
  - title: string         # Example title
    description: string   # What this example demonstrates
    code: string          # The actual code
    explanation: string   # How it works
```

## How to Contribute

Contributing is as simple as creating a YAML file.

### Step 1: Create Your Config File

Create a new file in the `/config/` directory following the naming pattern `your-tech.yaml`:

```yaml
# Example: config/nextjs.yaml
active: true
update_interval_days: 7
repo_url: https://github.com/vercel/next.js.git
paths:
  - docs
  - examples
```

### Step 2: Required Fields

Every config file must include:

| Field      | Required | Description                         | Example                               |
|------------|----------|-----------------------------------|-------------------------------------|
| `active`   | ✅       | Whether this config should be processed | `true`                          |
| `repo_url` | ✅       | Full GitHub repository URL         | `https://github.com/vercel/next.js.git` |
| `paths`    | ✅       | List of directory paths to include | `["docs", "examples"]`              |

### Step 3: Optional Configuration

Enhance your config with optional fields:

```yaml
active: true
update_interval_days: 7          # Optional: How often to update (defaults to 7)
repo_url: https://github.com/owner/repository.git
paths:
  - docs                          # Directory paths only (no specific files)
  - examples                      # No leading slashes
  - tutorials
```

## Best Practices for Configuration

### Choosing the Right Paths

Focus on directories with the most valuable content for AI assistance:

```yaml
# ✅ Recommended: Specific, high-value directories
paths:
  - docs                    # Documentation
  - examples                # Code examples
  - tutorials               # Learning materials
  - guides                  # How-to guides

# ❌ To Avoid: Too broad, low-value, or problematic directories
paths:
  - "/"                     # Root directory (not allowed)
  - tests                   # Usually not helpful for AI context
  - node_modules            # Dependencies (will be slow and unhelpful)
  - .git                    # Version control files
```

### Directory Path Guidelines

- **No leading slashes**: Use `docs` not `/docs/`
- **No trailing slashes**: Use `examples` not `examples/`
- **Directory names only**: Individual files are not supported yet
- **Relative to repository root**: Paths start from the repository’s main directory

## Contribution Workflow

### Making a Quick Contribution

1. **Fork this repository**
2. **Create your config file** in `/config/your-tech.yaml`
3. **Test locally** (optional but recommended):

   ```bash
   cd mcp-server && python update.py --config=../config/your-tech.yaml
   ```

4. **Submit a Pull Request** with:

   - Clear title: "Add [Technology Name] configuration"
   - Description of what content you’re adding
   - Why this technology would be valuable for AI assistance

## Pull Request Guidelines

When submitting your contribution:

### Title Format

- `Add [Technology]: Brief description`
- Example: `Add Prisma: Database toolkit and ORM`

### Description Template

```markdown
## Technology Addition

**Technology**: [Name]  
**Category**: [Category]  
**Repository**: [owner/repo]  

## Content Included
- [ ] Documentation
- [ ] Examples
- [ ] Tutorials
- [ ] API Reference

## Why This Addition?
Brief explanation of why this technology is valuable for AI assistance.

## Testing
- [ ] Config file follows the schema
- [ ] Paths are accessible and contain valuable content
- [ ] Local testing completed (if applicable)
```

## Use Cases

### For Developers

- Quick reference for syntax and patterns  
- Starting templates for new projects  
- Best practice examples across technologies  
- Cross-technology comparison and learning  

### For AI Assistants

- Rich context for more accurate code generation  
- Structured knowledge base for technology stacks  
- Consistent format for reliable parsing  
- Comprehensive examples for better understanding  

### For Teams

- Standardized patterns and practices  
- Onboarding materials for new technologies  
- Code review reference  
- Architecture decision support  

## Community Resources

- **Issues**: Report bugs or request new technology stacks  
- **Discussions**: Share ideas and ask questions  
- **Pull Requests**: Contribute improvements and additions  
- **Wiki**: Extended documentation and guides  

## Additional Contribution Information

Contributing is easy with a well-structured YAML file.

### Initial Config Setup

Create a file in `/config/` named `your-tech.yaml`:

```yaml
# Example: config/nextjs.yaml
active: true
update_interval_days: 7
repo_url: https://github.com/vercel/next.js.git
paths:
  - docs
  - examples
```

### Mandatory Fields Recap

Your config file must include:

| Field      | Required | Description                         | Example                               |
|------------|----------|-----------------------------------|-------------------------------------|
| `active`   | ✅       | Whether this config should be processed | `true`                          |
| `repo_url` | ✅       | Full GitHub repository URL         | `https://github.com/vercel/next.js.git` |
| `paths`    | ✅       | List of directory paths to include | `["docs", "examples"]`              |

### Optional Enhancements

Add optional fields to customize updates:

```yaml
active: true
update_interval_days: 7          # How often to update (default is 7)
repo_url: https://github.com/owner/repository.git
paths:
  - docs
  - examples
  - tutorials
```

## Recommended Path Selection

Stick to directories offering the best AI assistance potential:

```yaml
# ✅ Best: Highly relevant directories
paths:
  - docs
  - examples
  - tutorials
  - guides

# ❌ Avoid these
paths:
  - "/"                     # Root directory (not allowed)
  - tests
  - node_modules
  - .git
```

### Path Formatting Rules

- No leading slashes
- No trailing slashes
- Only directory names allowed (files unsupported)
- Paths relative to repo root

## Fast Contribution Tips

1. **Fork repository**  
2. **Add your config** at `/config/your-tech.yaml`  
3. **Optionally test locally**:

   ```bash
   cd mcp-server && python update.py --config=../config/your-tech.yaml
   ```

4. **Open a Pull Request**  
   - Provide a clear, concise title  
   - Explain what you’re adding and why  

## Pull Request Submission

### Title Style

- Use `Add [Technology]: Brief description`
- Example: `Add Prisma: Database toolkit and ORM`

### Pull Request Content

```markdown
## Technology Addition

**Technology**: [Name]  
**Category**: [Category]  
**Repository**: [owner/repo]  

## Content Included
- [ ] Documentation
- [ ] Examples
- [ ] Tutorials
- [ ] API Reference

## Why This Addition?
Explain why this technology is important for AI assistance.

## Testing
- [ ] Schema compliance
- [ ] Accessible content paths
- [ ] Completed local tests (if applicable)
```

## Community Engagement

- **Issues**: For bug reports and feature requests  
- **Discussions**: To share ideas and ask questions  
- **Pull Requests**: To submit improvements  
- **Wiki**: For extended docs and guides  

## License

MIT License — freely use it in personal and commercial projects.

## Acknowledgments

- Contributors expanding and maintaining the project  
- Community members inspiring content  
- AI developers enabling integration  

---

## Made with ❤️ for the developer community

*Awesome Context - Empowering AI-assisted development with curated, structured knowledge.*
