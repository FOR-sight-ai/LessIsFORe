# Less is FORe.html

**Less is FORe.html** is a minimalist, single-file agentic AI assistant. 
It is a web-based interface with a simple agent loop and the minimal set of tools.

You must connect it to an open-ai compatible API and select a folder - it then allows to answer questions based on the content of that folder (compatible with PDFs, Docx, PPTX, and text).

---

## 🚀 Key Features

* **Single-File Architecture:** The entire application (HTML, CSS, and JS) is contained in one file.
* **Local File Access:** Uses the File System Access API to read and analyze local directories (read-only).
* **Rich Format Support:** Built-in parsers for `.pdf`, `.docx`, `.pptx`, and standard text files.
* **Agentic Tools:** The assistant can list files, read specific lines, search content (grep-style), and perform parallel analysis across multiple files. The agentic loop is minimalist and framework-free.
* **Privacy-First:** No data is sent to a central server by the UI; it only communicates with the LLM API endpoint you configure.

---

## 🛡️ Why a Single File? 

In corporate or highly constrained environments, deploying new software is often a nightmare due to strict security policies, registry blocks, or the "no-install" rule.

**Less is FORe.html** answers most of these deployment challenges because:

1. **Zero Installation:** There is no executable to whitelist and no environment (like Python or Node.js) to configure.
2. **Auditability:** A single HTML file is transparent. A security officer can review the entire codebase in minutes.
3. **Isolation:** It runs within the browser sandbox. It cannot access your system beyond the specific folder you explicitly "Open" via the browser's permission prompt.
4. **No Persistence:** It doesn't leave "droppings" in system folders or registry keys. It does not have a write permission on the opened folder.

---

## ⚠️ Security Warnings

* **Local API Usage:** For maximum security, use this with a **local LLM API** (like Ollama, LocalAI, or vLLM). If you point this to a public cloud API, your document contents will be sent to that provider.
* **Browser Sandbox:** Do not disable browser security features. The application relies on standard web security to keep your environment safe.
* **Only open trusted sources folder:** **Prompt injections** attacks might be present in untrusted documents, designed to trick the UI.

---

## 🔗 LLM Backend & Proxying

This file acts as the **Frontend**. It requires an OpenAI-compatible API to function.

For a simple, configurable proxy to handle your LLM backends, we recommend looking at the **MunchFORsen** project. 
It pairs perfectly with this UI to provide a full-stack, corporate-compatible AI experience.

## Acknowledgement

This project received funding from the French ”IA Cluster” program within the Artificial and Natural Intelligence Toulouse Institute (ANITI) and from the "France 2030" program within IRT Saint Exupery. The authors gratefully acknowledge the support of the FOR projects.

## 📜 License

This project is open source, under the MIT license.
