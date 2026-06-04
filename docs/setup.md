# Setup Guide

**Last Updated:** June 4, 2026

---

## Prerequisites

Before you begin, make sure you have:

- [ ] GitHub account (for the public build)
- [ ] OpsDex account (the platform we're migrating to)
- [ ] Basic understanding of AI agents and workflows
- [ ] Git installed
- [ ] Terminal/command line access

---

## Step 1: Clone the Repository

```bash
git clone https://github.com/Abi5678/hermes-migration-to-opdex.git
cd hermes-migration-to-opdex
```

---

## Step 2: Setup OpsDex

### What is OpsDex?

OpsDex is an AI agent orchestration platform that provides:

- **Agent management** - Define and manage multiple AI agents
- **Workflow orchestration** - Connect agents into cohesive workflows
- **Integration support** - Connect to GitHub, Slack, email, and more
- **Observability** - Monitor agent performance and behavior
- **Documentation** - Built-in documentation and tooling

### OpsDex Setup Steps

1. **Create OpsDex Account**
   - Visit: https://opdex.io
   - Sign up for a free account
   - Verify your email

2. **Create a New Project**
   - Go to "Projects" in OpsDex
   - Click "Create New Project"
   - Name it: "Hermes Migration"
   - Select "Public" visibility

3. **Generate API Keys**
   - Go to "Settings" > "API Keys"
   - Create a new API key
   - Copy the key (you'll need it for setup)

4. **Install OpsDex CLI**
   ```bash
   # macOS
   brew install opdex-cli

   # Linux
   curl -fsSL https://opdex.io/install.sh | bash

   # Verify installation
   opdex --version
   ```

5. **Login to OpsDex**
   ```bash
   opdex login
   # Follow the prompts to authenticate
   ```

6. **Link Your Project**
   ```bash
   opdex link hermes-migration
   # This will connect your local project to OpsDex
   ```

---

## Step 3: Configure Your Environment

Create a `.env` file in the project root:

```bash
cp .env.example .env
```

Edit `.env` with your OpsDex API key:

```env
OPDEX_API_KEY=your_api_key_here
OPDEX_PROJECT_ID=your_project_id_here
OPDEX_ENVIRONMENT=production
```

---

## Step 4: Install Dependencies

```bash
# Install Node.js dependencies (if using JavaScript/TypeScript)
npm install

# Or Python dependencies (if using Python)
pip install -r requirements.txt
```

---

## Step 5: Initialize the Project

```bash
# Initialize OpsDex integration
opdex init

# This will:
# - Create necessary configuration files
# - Setup CI/CD pipeline
# - Configure agent definitions
# - Create workflow templates
```

---

## Step 6: Run Initial Setup

```bash
# Run setup script
opdex setup

# This will:
# - Create required directories
# - Setup testing infrastructure
# - Configure logging
# - Initialize database (if needed)
```

---

## Step 7: Verify Installation

```bash
# Check OpsDex connection
opdex status

# Expected output:
# ✓ OpsDex connected
# ✓ Project linked
# ✓ Environment configured
# ✓ All services running
```

---

## Step 8: Start Building

Now you're ready to start building! Check the architecture guide to understand the project structure.

---

## Troubleshooting

### Issue: "OpsDex CLI not found"
**Solution:** Make sure you installed the CLI correctly and it's in your PATH.

### Issue: "API key not valid"
**Solution:** Check that you copied the API key correctly and it hasn't expired.

### Issue: "Project not linked"
**Solution:** Run `opdex link hermes-migration` again to link your project.

### Issue: "Connection refused"
**Solution:** Check that OpsDex is running and your firewall allows connections.

---

## Next Steps

- [ ] Read the [Architecture Guide](architecture.md)
- [ ] Explore [Agent Definitions](../src/agents/)
- [ ] Check [Workflow Orchestration](../src/workflows/)
- [ ] Join the [Community](#)

---

## Getting Help

- **Docs:** https://opdex.io/docs
- **GitHub Issues:** https://github.com/Abi5678/hermes-migration-to-opdex/issues
- **Discord:** https://discord.gg/opdex

---

**Need help?** Open an issue on GitHub and I'll get back to you!
