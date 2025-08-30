
````markdown
 ____                   __ _                  ____               
|  _ \  __ _ _ __ __ _ / _| | _____      __  / ___|___  _ __ ___ 
| | | |/ _` | '__/ _` | |_| |/ _ \ \ /\ / / | |   / _ \| '__/ _ \
| |_| | (_| | | | (_| |  _| | (_) \ V  V /  | |__| (_) | | |  __/
|____/ \__,_|_|  \__,_|_| |_|\___/ \_/\_/    \____\___/|_|  \___|
````

# Daraflow

**A Prompt to AI File Semantic Parser**
Daraflow lets you transform *Prompts* into **ready-to-use APIs**, capable of receiving documents and returning structured JSON output — no coding required.

Open Source Project licensed under **AGPLv3** to ensure it always remains free and that any SaaS use must share its improvements with the community.

---

## Features

* **Prompt → API**: Define a prompt and Daraflow automatically creates a REST endpoint.
* **Flexible input**: Send files (PDF, TXT, DOCX, CSV, JSON, etc.).
* **Semantic interpretation** powered by LLMs (Gemini, OpenAI, OSS models).
* **Structured JSON output** ready for your app or system.
* **Docker Ready**: quick deployment anywhere.
* **Simple UI**: create, test, and manage APIs through a graphical interface.

---

## Installation

### Option 1: Docker

```bash
docker run -d \
  --name daraflow \
  -p 8080:8080 \
  ghcr.io/daraflow/daraflow:latest
```

### Option 2: Clone and run locally

```bash
git clone https://github.com/your-org/daraflow.git
cd daraflow
make run
```

---

## Basic Usage

1. Open the **Daraflow UI** at [http://localhost:8080](http://localhost:8080).
2. Create a **Prompt Parser** (example: "Extract financial fields from the document").
3. Daraflow automatically generates a **REST endpoint**.
4. Send a file to the endpoint and get back structured JSON.

Example with `curl`:

```bash
curl -X POST http://localhost:8080/api/parse/financial \
  -F "file=@balance.pdf"
```

Response:

```json
{
  "company": "Digital Services Ltd.",
  "year": 2024,
  "income": 152000.75,
  "expenses": 98000.40,
  "net_profit": 54000.35
}
```

---

## 🛠Roadmap

* [ ] Multi-tenant support.
* [ ] Monitoring dashboards.
* [ ] Native connectors (Google Drive, Dropbox, MinIO).
* [ ] Predefined prompt templates (financial, legal, medical).
* [ ] CLI for automation.

---

## Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/new-feature`.
3. Commit your changes: `git commit -m "Add new feature"`.
4. Push the branch: `git push origin feature/new-feature`.
5. Open a Pull Request.

Please check [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE\_OF\_CONDUCT.md](CODE_OF_CONDUCT.md).

---

## License

This project is licensed under **AGPLv3**.
That means:

* You can use, modify, and redistribute the code.
* If you use it as a **network service (SaaS)** and modify it, you must also share your modifications.

---

## Daraflow Enterprise

We provide an **Enterprise Edition** with additional features:

* Advanced multi-tenancy.
* Kubernetes cluster scalability.
* SSO/LDAP integration.
* Security and auditing modules.
* Dedicated support & SLA.

Contact us at **[contact@daraflow.com](mailto:contact@daraflow.com)** for more details.

---

## Community

* 💬 Join the community on Discord (link coming soon).
* 📢 Follow us on [Twitter/X](https://twitter.com/) for updates.
* 📝 Share your ideas through Issues and Pull Requests.

---

Made with ❤️ by [SedeSoft](https://sedesoft.com) & the community.
