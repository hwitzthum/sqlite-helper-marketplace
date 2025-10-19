# SQLite Helper Plugin for Claude Code

A comprehensive Claude Code plugin for implementing SQLite databases with SQLAlchemy in Python. This plugin provides interactive guidance, best-practice code generation, and database operation support.

## Features

- **Interactive Database Design**: Ask questions to understand your requirements
- **SQLAlchemy Best Practices**: Generate production-ready ORM models
- **Connection Management**: Proper session handling and connection pooling
- **Migration Support**: Alembic integration guidance
- **Query Optimization**: Performance tips and N+1 query prevention
- **Testing Support**: Generate test fixtures and test database setup
- **Security**: SQL injection prevention and parameterized queries

## Installation

### From Marketplace
```bash
# Add the marketplace (if hosting on GitHub)
/plugin marketplace add your-username/sqlite-helper-plugin

# Install the plugin
/plugin install sqlite-helper
```

### Local Installation
```bash
# Clone or copy the plugin to your local plugins directory
cp -r sqlite-helper-plugin ~/.claude/plugins/

# Restart Claude Code
```

## Available Commands

### `/sqlite-init`
Initialize a new SQLite database project with SQLAlchemy setup.

**Usage:**
```bash
/sqlite-init
```

This will ask you questions about your project and generate:
- Database connection configuration
- Base model class with best practices
- Session management utilities
- Example model

### `/sqlite-model`
Create a new SQLAlchemy model with proper relationships and constraints.

**Usage:**
```bash
/sqlite-model
```

Generates models with:
- Proper column types and constraints
- Relationship definitions
- Indexes for performance
- Validation methods
- Repr and str methods

### `/sqlite-query`
Get help with SQLAlchemy queries and best practices.

**Usage:**
```bash
/sqlite-query
```

Provides guidance on:
- Efficient querying patterns
- Eager vs lazy loading
- Avoiding N+1 queries
- Pagination
- Aggregations and joins

### `/sqlite-migrate`
Set up Alembic migrations for your SQLite database.

**Usage:**
```bash
/sqlite-migrate
```

Helps with:
- Alembic initialization
- Creating migrations
- Applying migrations
- Rolling back changes

### `/sqlite-test`
Generate test fixtures and test database setup.

**Usage:**
```bash
/sqlite-test
```

Creates:
- Test database configuration
- Fixture factories
- Example test cases
- Cleanup utilities

## Available Agents

### `sqlite-architect`
A specialized agent for database design and schema optimization. Great for complex database design discussions and refactoring existing schemas.

**How to use:**
```bash
/agents
# Select sqlite-architect from the list
```

### `sqlite-debugger`
Expert at diagnosing and fixing SQLite and SQLAlchemy issues.

**How to use:**
```bash
/agents
# Select sqlite-debugger from the list
```

## Quick Start Example
```bash
# 1. Initialize your project
/sqlite-init

# 2. Create your first model
/sqlite-model

# 3. Get help with queries
/sqlite-query

# 4. Set up migrations
/sqlite-migrate

# 5. Create tests
/sqlite-test
```

## Best Practices Included

This plugin ensures your SQLite implementation follows these best practices:

1. **Connection Management**: Proper use of context managers and session cleanup
2. **Type Safety**: Appropriate SQLAlchemy column types for SQLite
3. **Indexes**: Automatic index suggestions for foreign keys and frequently queried columns
4. **Transactions**: Proper transaction handling and rollback on errors
5. **Security**: Parameterized queries to prevent SQL injection
6. **Testing**: Isolated test databases and proper fixture cleanup
7. **Performance**: Query optimization tips and N+1 query prevention
8. **Migrations**: Version-controlled schema changes with Alembic

## Requirements

Your Python environment should have:
- Python 3.8+
- SQLAlchemy 2.0+ (the plugin will suggest installation if needed)
- Alembic (optional, for migrations)

## Common Workflows

### Starting a New Project
```bash
/sqlite-init
# Follow the interactive prompts
```

### Adding a New Table
```bash
/sqlite-model
# Describe your table requirements
```

### Optimizing Queries
```bash
/sqlite-query
# Paste your current query for optimization suggestions
```

### Database Refactoring
```bash
/agents
# Select sqlite-architect
# Describe your refactoring needs
```

## Support

For issues, questions, or contributions:
- File issues on the GitHub repository
- Use `/bug` in Claude Code to report plugin issues
- Check the official SQLAlchemy documentation: https://docs.sqlalchemy.org/

## License

MIT License - See LICENSE file for details.

## Version History

### 1.0.0 (Initial Release)
- Interactive database initialization
- Model generation with best practices
- Query optimization guidance
- Migration setup support
- Test database utilities
- Two specialized agents (architect and debugger)
- 