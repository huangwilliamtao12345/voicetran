
#### Quick Install 
```bash
# Clone and install
git clone https://github.com/huangwilliamtao12345/voicetran
cd voicetran
chmod +x install.sh  # Make install script executable
./install.sh

# Run interactive setup
vtrans --setup

# Start using voicetran
vtrans
```

### Configuration

#### Get Your API Keys

1. **Fireworks API Key** (for transcription - recommended):
   - Get your free key at: https://app.fireworks.ai/settings/users/api-keys
   - Sign up for free, no credit card required
   - Provides ultra-fast transcription (23x faster than OpenAI)

2. **Google Gemini API Key** (for translation):
   - Get your free key at: https://aistudio.google.com/apikey
   - Sign up for free, no credit card required
   - Uses Gemini 2.5 Flash Lite Preview for fast, cost-effective translation

**Option A: Interactive Setup (Easiest)**
```bash
vtrans --setup
```

**Option B: Using config.json**
```bash
# Copy the template in your working directory
cp /path/to/voicetran/config.json.template config.json

# Edit config.json with your API keys
nano config.json  # or use your preferred editor
```

### Config File Structure
```json
{
  "fireworks_api_key": "your-key-here",
  "openai_api_key": "your-key-here",
  "default_target_language": "zh",
  "theme": "dark",
  "sensitivity_mode": "Balanced",
  "use_turbo_model": true,
  "use_vad_optimization": true,
  "show_history": true,
  "show_stats": true
}
```

## Session Output

Sessions are saved with timestamps in the format:
```
voice_translation_YYYYMMDD_HHMMSS.txt
```

## Uninstallation

To remove voicetran from your system:

```bash
cd voicetran
./uninstall.sh
```

## Requirements

- Python 3.8+
- macOS/Linux
- Working microphone
- Internet connection
- API keys (Fireworks AI and/or OpenAI)


