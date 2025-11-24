# Homebrew Tap for Minimal Timer

This is a [Homebrew](https://brew.sh) tap for [minimal-timer](https://github.com/dandaniel5/minimal-timer) - a minimalist command-line timer with smart time parsing.

## Installation

```bash
brew tap dandaniel5/timer
brew install timer
```

## What is Minimal Timer?

A powerful yet minimal command-line timer that supports:

- ⏰ **Smart time parsing** - `10m`, `1h 30s`, `2d 5h`
- 📝 **Named timers** - Add labels with `-n` flag
- 💤 **Sleep integration** - Auto-sleep system or display
- 📋 **Multiple timers** - Run and track multiple timers
- 🔔 **Audio notifications** - Bell sound on completion

## Quick Start

```bash
# Simple 10 minute timer
timer 10m

# Named timer with system sleep
timer 25m -n "Pomodoro" -s

# List all running timers
timer -ls
```

## Full Documentation

For complete documentation, examples, and advanced usage, visit:
https://github.com/dandaniel5/minimal-timer

## Features

### Smart Time Parsing
Supports natural language time input with multiple units:
- Seconds: `s`, `sec`, `second`, `seconds`
- Minutes: `m`, `min`, `minute`, `minutes` (default)
- Hours: `h`, `hour`, `hours`
- Days: `d`, `day`, `days`
- Weeks: `w`, `week`, `weeks`
- Years: `y`, `year`, `years`

### Command-Line Options

```
-n, --name NAME       Timer name/label
-s, --sleep           Sleep system after timer
-sd, --sleep-display  Sleep display only after timer
-ls, --list           List all running timers
```

### Examples

```bash
# Basic timer (defaults to minutes)
timer 5

# Complex duration
timer 1h 30m 45s

# Named timer
timer 25m -n "Work session"

# Multiple timers
timer 1h -n "Meeting" &
timer 30m -n "Lunch" &
timer -ls

# Auto-sleep display after timer
timer 20m -n "Break" -sd
```

## Use Cases

**Pomodoro Technique**
```bash
timer 25m -n "Focus" && timer 5m -n "Break"
```

**Meeting Reminders**
```bash
timer 1h -n "Team Standup" -s
```

**Cooking**
```bash
timer 12m -n "Pasta" &
timer 15m -n "Sauce" &
```

**Screen Breaks**
```bash
timer 20m -n "Eye Rest" -sd
```

## Requirements

- Python 3.6+
- macOS (for sleep functionality)

## Support

- **Issues**: https://github.com/dandaniel5/minimal-timer/issues
- **Source**: https://github.com/dandaniel5/minimal-timer

## License

MIT License - see the [main repository](https://github.com/dandaniel5/minimal-timer) for details.
