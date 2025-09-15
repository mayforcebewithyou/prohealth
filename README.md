# Coming Soon — Flask demo

This is a minimal Flask app that serves a modern "coming soon" landing page with a countdown and email subscription endpoint. It's intentionally dependency-light and uses only Flask.

Quick start (macOS / zsh):

1. Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the app:

```bash
python app.py
```

4. Open http://127.0.0.1:5001

Notes
- This example stores subscribers in memory; for production wire up a database or external email service.
- The launch date is currently set to the server's UTC midnight; edit `app.py` to set a fixed launch datetime.


kill app: lsof -t -iTCP:5001 -sTCP:LISTEN -n -P | xargs -r kill -9; sleep 0.2; lsof -iTCP:5001 -sTCP:LISTEN -n -P || true

run app: cd '/Users/santu/Desktop/Health App/code' && source .venv/bin/activate && python app.py