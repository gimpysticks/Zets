# Zets Workflow - Saving Warp Output to Markdown

2025-06-22 02:51:30

## Quick Commands

- `sz <filename> [title]` - Create new markdown file
- `az <filename>` - Append content to existing file  
- `lz [pattern]` - List all zets files
- `vz` - View zets directory

## Workflow Steps

### 1. Copy Content from Warp
- Select and copy the output block from Warp (Ctrl+C)

### 2. Create New Zets File
```bash
sz filename "Optional Title"
# Example: sz docker_commands "Docker Reference"
```

### 3. Paste Content
- The editor will open automatically
- Paste your content (Ctrl+V)
- Save and exit

### 4. Alternative: Direct Paste
```bash
# Create file first
sz filename "Title"

# Then append copied content
az filename
# Paste content and press Ctrl+D when done
```

### 5. Quick Append to Existing File
```bash
az existing_filename
# Paste new content and press Ctrl+D
```

### 6. Browse Your Zets
```bash
lz                    # List all files
lz "*docker*"         # List files matching pattern
vz                    # View directory contents
```

## File Organization

Files are stored in `~/zets/` with:
- Automatic `.md` extension
- Timestamp headers
- Proper markdown formatting
- Searchable content

## Advanced Usage

### Using Heredoc for Large Content
```bash
cat >> ~/zets/filename.md << 'EOF'
Your content here
Multiple lines
EOF
```

### Direct Command Output Capture
```bash
# Save command output directly
command_output > ~/zets/command_results.md
```

### Integration with Git (Optional)
```bash
cd ~/zets
git init
git add .
git commit -m "Added new zets"
```
