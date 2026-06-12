# Setup Guide

## Prerequisites

You need:

- n8n installed or n8n Cloud
- Ollama installed locally
- Llama 3 model pulled in Ollama
- IMAP email account credentials

## Install Ollama Model

Run:

```bash
ollama pull llama3:8b
```

Start Ollama:

```bash
ollama serve
```

## Configure n8n Credentials

In n8n, create an IMAP credential for the inbox you want to monitor.

## Import Workflow

1. Open n8n.
2. Go to Workflows.
3. Choose Import from File.
4. Select `workflow.json`.
5. Reconnect your own credentials.
6. Test each node before activating the workflow.

## Important

This workflow prepares drafts for review. Do not enable automatic sending until you have added human approval and tested the workflow carefully.
