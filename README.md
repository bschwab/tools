# Tools

A collection of utilities and test tools.

## Projects

### Ollama Load Test

Overnight benchmark tool for testing Ollama models with real-time performance metrics and clean progress visualization.

**Features:**
- Clean progress bar during generation (no text clutter)
- Real-time token counting and TPS tracking
- Peak throughput measurement
- JSONL and CSV logging for analysis
- Configurable model parameters (temperature, context size, etc.)

**Usage:**
```bash
cd ollama-load-test
pip install -r requirements.txt
python ollama-test.py --iterations 10
```

**Environment Variables:**
- `OLLAMA_HOST` - Ollama server URL (default: `http://127.0.0.1:11434`)
- `OLLAMA_MODEL` - Model to test (default: `gpt-oss:20b`)

**Example Output:**
```
[██████████████████████████████] 1490tok | 74.0 t/s | peak 76.3 | 20.1s
✓ 1490 tokens | 74.0 t/s (peak 76.3) | 20.1s
```

See [`ollama-load-test/ollama-test.py`](./ollama-load-test/ollama-test.py) for all available options.

