# Cisco Configuration Diff Generator

A Python script for generating human-readable diffs between Cisco device configurations. This tool helps network administrators easily identify changes between different versions of device configurations.

## Features

- Generates clear, readable diff files highlighting changes between configurations
- Identifies modified, added, and removed lines
- Includes contextual information around changes
- Handles file validation and error checking
- Supports custom output file names and context line count

## Usage

```bash
python config_diff.py old_config.txt new_config.txt [--output diff.txt] [--context 10]
```

### Arguments

- `old_file`: Path to the original configuration file
- `new_file`: Path to the new configuration file
- `--output`: Optional path for the output diff file
- `--context`: Number of context lines to show (default: 10)

### Example Output

```
(Context): interface GigabitEthernet0/1
(Modified): description Primary Link # Modified
(Added): bandwidth 1000000
(Removed): no shutdown
```

## Requirements

- Python 3.6+

## Error Handling

The script includes comprehensive error handling for common scenarios:

- Missing input files
- Empty files
- Files with different extensions
- Non-text files
- Unsupported encodings

## Integration

This script can be integrated into larger automation workflows or used as a standalone tool. The diff format is designed to be both human-readable and machine-parseable.