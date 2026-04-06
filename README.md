🔐 Login Log Parser

A simple Python project for parsing login logs, detecting failed attempts, and identifying suspicious IP activity.
This project is designed to reinforce Python fundamentals while simulating a basic security monitoring tool.

⸻
```
📌 Features
	•	Parse raw login log lines into structured data
	•	Load and process log files
	•	Count failed login attempts per IP
	•	Detect suspicious IPs based on a threshold
	•	Generate a human-readable summary report
```
⸻

📂 Project Structure

```

login-log-parser/
│
├── src/
│   ├── parser.py          # parse_log_line, load_log
│   ├── analysis.py        # failures_by_ip, top_offenders
│   ├── report.py          # summary_report
│
├── tests/
│   └── test_analysis.py   # pytest tests
│
├── sample.log             # example log file
├── README.md
├── requirements.txt

```
⸻

🧠 Data Format

Each log entry is represented as a dictionary:
```
{
    "ip": "192.168.1.1",
    "user": "admin",
    "success": False,
    "time": "08:01"
}
```

⸻

⚙️ Core Functions
```
parse_log_line(line: str) -> dict

Parses a single log line into a structured dictionary.

load_log(filepath: str) -> list[dict]

Reads a log file and returns a list of parsed entries.

failures_by_ip(logs: list[dict]) -> dict[str, int]

Counts failed login attempts grouped by IP address.

top_offenders(logs: list[dict], threshold: int) -> list[str]

Returns a list of IPs with failed attempts above a given threshold.

summary_report(logs: list[dict]) -> str

Generates a readable summary of login activity.
```
⸻

🧪 Installation & Setup

# Clone the repository
git clone https://github.com/your-username/login-log-parser.git

# Navigate into the project
cd login-log-parser

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt


⸻

▶️ Usage

python src/main.py sample.log


⸻

📊 Example Output
```
Total logins: 5
Failed logins: 4

Failures by IP:
192.168.1.1 → 2
10.0.0.5 → 2

Top offenders (threshold = 2):
192.168.1.1
10.0.0.5

```
⸻

🧪 Running Tests

pytest


⸻
```
🛠️ Development Tools
	•	ruff → linting
	•	mypy → static type checking
	•	bandit → security analysis
	•	pytest → testing

ruff check .
mypy .
bandit -r .
```

⸻

🔐 Security Perspective

This project demonstrates a basic intrusion detection pattern:
	•	Detect repeated failed login attempts
	•	Identify potential brute-force attacks
	•	Analyze login behavior by IP address

⸻

📈 Future Improvements
	•	Add real-time log monitoring
	•	Integrate with a database
	•	Add visualization (charts/dashboard)
	•	Export reports to JSON/CSV
	•	Add CLI arguments (threshold, filters)

⸻

🧾 License

MIT License

⸻

👤 Author

Your Name
GitHub: https://github.com/your-username

⸻

💡 Notes

This project focuses on:
	•	Python data structures (lists, dicts, sets, tuples)
	•	Comprehensions and sorting
	•	File handling
	•	Basic security analysis concepts

⸻
