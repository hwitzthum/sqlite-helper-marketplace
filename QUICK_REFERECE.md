# SQLite Helper Plugin - Quick Reference

## 🚀 Installation

```bash
# Local installation
cp -r sqlite-helper-plugin ~/.claude/plugins/
/plugin install sqlite-helper

# From GitHub (when hosted)
/plugin marketplace add username/sqlite-helper-plugin
/plugin install sqlite-helper
```

## 📋 Commands Overview

| Command | Purpose | When to Use |
|---------|---------|-------------|
| `/sqlite-init` | Setup new project | Starting from scratch |
| `/sqlite-model` | Create models | Adding database tables |
| `/sqlite-query` | Query help | Writing/optimizing queries |
| `/sqlite-migrate` | Setup migrations | Schema version control |
| `/sqlite-test` | Testing setup | Adding test coverage |

## 🤖 Agents Overview

| Agent | Expertise | When to Use |
|-------|-----------|-------------|
| `sqlite-architect` | Design & optimization | Complex schemas, refactoring |
| `sqlite-debugger` | Error diagnosis | Something's broken |

## 💡 Common Workflows

### Starting a New Project
```bash
/sqlite-init
# Answer questions about your project
# Get: database.py, models/base.py, main.py

/sqlite-model
# Describe your first model
# Get: Complete model with relationships

/sqlite-migrate
# Set up Alembic
# Get: Migration configuration

/sqlite-test
# Set up testing
# Get: Test fixtures and examples
```

### Optimizing Existing Code
```bash
/sqlite-query
# Show your slow query
# Get: Optimized version + explanation
```

### Complex Design Decisions
```bash
/agents
# Select: sqlite-architect
# Discuss: Schema design, normalization, etc.
# Get: Expert guidance through dialogue
```

### Debugging Errors
```bash
/agents
# Select: sqlite-debugger
# Share: Error message and code
# Get: Diagnosis and fix
```

## 🎯 What Each Command Asks

### `/sqlite-init`
- What kind of application?
- Project structure preferences?
- SQLAlchemy version?
- Connection pooling needs?
- Database file location?

### `/sqlite-model`
- What does this model represent?
- What fields are needed?
- Data types for each field?
- Any relationships?
- Validation rules?
- Which fields to index?

### `/sqlite-query`
- What are you trying to retrieve?
- Current query (if any)?
- Performance issues?
- Expected result?

### `/sqlite-migrate`
- Already have Alembic setup?
- Existing tables to track?
- Project structure?
- Team size?

### `/sqlite-test`
- Testing framework?
- Current tests?
- What to test?
- Need realistic data?

## 📚 What You Get

### From `/sqlite-init`
- `database.py` - Connection config, session management
- `models/base.py` - Base model with timestamps
- `main.py` - Example usage
- `requirements.txt` - Dependencies

### From `/sqlite-model`
- Complete model class
- Proper column types
- Relationships configured
- Indexes added
- Validation methods
- Usage examples

### From `/sqlite-query`
- Query patterns (filter, join, aggregate)
- Optimization techniques
- N+1 query prevention
- Pagination examples
- Security best practices

### From `/sqlite-migrate`
- Alembic configuration
- Migration workflow
- Common operations guide
- Troubleshooting help

### From `/sqlite-test`
- Test database setup
- Factory functions
- Example test cases
- pytest configuration

## ⚡ Best Practices Built-In

✅ Foreign keys always enabled  
✅ Context managers for sessions  
✅ Timestamps on all models  
✅ Indexes on foreign keys  
✅ Validation decorators  
✅ SQL injection prevention  
✅ Isolated test databases  
✅ Proper migrations  

## 🔧 SQLite-Specific Features

- **Type Affinity** handling
- **Foreign Key** enforcement (PRAGMA)
- **Batch Mode** for migrations
- **Thread Safety** configuration
- **WAL Mode** suggestions
- **Connection Pooling** setup

## 📖 Example Interactions

### Quick Project Setup
```bash
User: /sqlite-init
Plugin: What kind of application?
User: Web app with user authentication
Plugin: [Asks more questions]
Plugin: [Generates complete setup]
```

### Model Creation
```bash
User: /sqlite-model
Plugin: What does this model represent?
User: Blog posts with comments
Plugin: [Asks about fields and relationships]
Plugin: [Generates Post and Comment models]
```

### Query Optimization
```bash
User: /sqlite-query
User: This query is slow: [shows code]
Plugin: I see the N+1 problem!
Plugin: [Shows optimized version with eager loading]
Plugin: Expected improvement: 100x faster
```

### Getting Expert Advice
```bash
User: /agents → sqlite-architect
User: Should I normalize this data?
Agent: Let's think through the trade-offs...
Agent: [Socratic dialogue about design choices]
```

### Debugging
```bash
User: /agents → sqlite-debugger
User: Getting IntegrityError on users.email
Agent: This means duplicate email...
Agent: [Provides diagnosis, fix, and prevention]
```

## 🎓 Learning Path

1. **Beginner**: Start with `/sqlite-init` and `/sqlite-model`
2. **Intermediate**: Learn `/sqlite-query` and `/sqlite-migrate`
3. **Advanced**: Use agents for complex discussions
4. **Expert**: Combine all tools for production systems

## 🔍 Troubleshooting

**Commands not showing?**
```bash
/help  # Check if /sqlite-* commands are listed
/plugin  # Verify sqlite-helper is installed
```

**Agents not available?**
```bash
/agents  # Look for sqlite-architect and sqlite-debugger
```

**Need to reinstall?**
```bash
/plugin uninstall sqlite-helper
/plugin install sqlite-helper
# Restart Claude Code
```

## 📦 Plugin Contents

```
sqlite-helper-plugin/
├── .claude-plugin/plugin.json    # Metadata
├── commands/                     # 5 slash commands
│   ├── sqlite-init.md
│   ├── sqlite-model.md
│   ├── sqlite-query.md
│   ├── sqlite-migrate.md
│   └── sqlite-test.md
├── agents/                       # 2 specialized agents
│   ├── sqlite-architect.md
│   └── sqlite-debugger.md
├── README.md                     # Full documentation
└── INSTALLATION.md              # Setup guide
```

## 🎯 Key Features

- **Interactive**: Asks questions to understand your needs
- **Educational**: Teaches principles, not just code
- **Complete**: Generates production-ready code
- **Best Practices**: Follows industry standards
- **SQLite-Optimized**: Handles SQLite quirks properly
- **Comprehensive**: Covers entire dev lifecycle

## 💬 Get Help

- **In commands**: They guide you with questions
- **With agents**: Deep discussions on complex topics
- **Documentation**: README.md and INSTALLATION.md

---

**Ready to start? Try `/sqlite-init` now!** 🚀
