# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a collection of custom slash commands for Claude Code that implement a task-based development workflow. The commands provide a structured approach to software development with four distinct phases: initialization, design, planning, and implementation.

## Command Architecture

The repository contains four interconnected slash commands that work together:

1. **task-init.md** - Creates task environment and requirements gathering
2. **task-design.md** - Analyzes existing systems and creates technical design
3. **task-todo.md** - Breaks down design into actionable development tasks
4. **task-develop.md** - Executes implementation based on todo list

## Task Management Structure

Each task follows a standardized directory structure:
```
.claude/tasks/{task_name}/
├── requirements.md  # Requirements definition
├── design.md       # Technical design
└── todo.md         # Implementation todo list
```

## Key Command Behaviors

### /task-init {task_name}
- Creates `.claude/tasks/{task_name}/` directory structure
- Generates templated requirements.md with sections for overview, background, functional/non-functional requirements, impact analysis, constraints, and system relationships
- Creates empty design.md and todo.md files

### /task-design {task_name}
- Reads requirements.md to understand task scope
- Analyzes existing project structure to maintain consistency
- Creates comprehensive design.md covering architecture, components, file structure, data design, API design, error handling, testing strategy, and performance/security considerations

### /task-todo {task_name}
- Reads design.md to understand technical requirements
- Creates structured todo.md with implementation order, task breakdown, deliverables, priorities, time estimates, and checkpoints
- Considers dependencies and development efficiency

### /task-develop {task_name}
- Reads both design.md and todo.md
- Implements tasks sequentially following the todo list
- Maintains code quality, follows existing patterns, includes appropriate tests
- Reports progress after each task completion

## Installation Method

Commands are installed by copying the .md files to the Claude Code commands directory:
```bash
cp claude-code-task-commands/*.md ~/.claude/commands/
```

## Language Support

The commands support Japanese language for requirements definition and design documentation while maintaining English compatibility for technical implementation.

## Development Philosophy

- **Staged Development**: Sequential progression through requirements → design → planning → implementation
- **Quality Focus**: Emphasizes code quality, maintainability, and integration with existing systems
- **Progress Tracking**: Concrete todo lists for work management
- **Consistency**: Respects existing code patterns and conventions