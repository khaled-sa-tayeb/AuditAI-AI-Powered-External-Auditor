<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
    <meta charset="UTF-8">
    <title>AuditAI — AI-Powered External Auditor</title>
    <style>
        :root {
            --color-canvas-default: #ffffff;
            --color-canvas-subtle: #f6f8fa;
            --color-border-default: #d0d7de;
            --color-border-muted: #d8dee4;
            --color-fg-default: #24292f;
            --color-fg-muted: #57606a;
            --color-accent-fg: #0969da;
            --color-accent-subtle: #ddf4ff;
            --color-neutral-muted: rgba(175, 184, 193, 0.2);
            --font-stack: -apple-system, BlinkMacSystemFont, "Segoe UI", "Noto Sans", Helvetica, Arial, sans-serif;
            --font-mono: ui-monospace, SFMono-Regular, SF Mono, Menlo, Consolas, Liberation Mono, monospace;
        }

        body {
            font-family: var(--font-stack);
            color: var(--color-fg-default);
            background-color: var(--color-canvas-default);
            line-height: 1.5;
            font-size: 16px;
            padding: 40px;
            max-width: 900px;
            margin: 0 auto;
        }

        h1, h2, h3 {
            border-bottom: 1px solid var(--color-border-muted);
            padding-bottom: 0.3em;
            margin-top: 24px;
            margin-bottom: 16px;
            font-weight: 600;
        }

        h1 { font-size: 2em; border-bottom: none; }
        h2 { font-size: 1.5em; }
        h3 { font-size: 1.25em; border-bottom: none; }

        p, ul {
            margin-top: 0;
            margin-bottom: 16px;
        }

        ul {
            padding-left: 2em;
        }

        li {
            margin-bottom: 0.25em;
        }

        blockquote {
            padding: 0 1em;
            color: var(--color-fg-muted);
            border-left: 0.25em solid var(--color-border-default);
            margin: 0 0 16px 0;
        }

        hr {
            height: 0.25em;
            padding: 0;
            margin: 24px 0;
            background-color: var(--color-border-muted);
            border: 0;
        }

        table {
            width: 100%;
            margin-bottom: 16px;
            border-collapse: collapse;
            border-spacing: 0;
        }

        table th, table td {
            padding: 6px 13px;
            border: 1px solid var(--color-border-default);
        }

        table tr {
            background-color: var(--color-canvas-default);
            border-top: 1px solid var(--color-border-muted);
        }

        table tr:nth-child(2n) {
            background-color: var(--color-canvas-subtle);
        }

        code, pre {
            font-family: var(--font-mono);
            font-size: 85%;
        }

        code {
            padding: 0.2em 0.4em;
            margin: 0;
            background-color: var(--color-neutral-muted);
            border-radius: 6px;
        }

        pre {
            padding: 16px;
            overflow: auto;
            font-size: 85% !important;
            line-height: 1.45;
            background-color: var(--color-canvas-subtle);
            border-radius: 6px;
            border: 1px solid var(--color-border-muted);
        }

        pre code {
            background-color: transparent;
            padding: 0;
        }

        .badges img {
            height: 20px;
            margin-right: 4px;
            vertical-align: middle;
        }
    </style>
</head>
<body>

    <h1>📄 AuditAI — AI-Powered External Auditor</h1>

    <blockquote>
        <p>Intelligent financial auditing system automating reconciliation, anomaly detection, and OCR invoice validation for enterprise-level audit operations.</p>
    </blockquote>

    <div class="badges">
        <img src="https://img.shields.io/badge/Status-Complete-brightgreen" alt="Status">
        <img src="https://img.shields.io/badge/Python-3.10-blue" alt="Python">
        <img src="https://img.shields.io/badge/KAU-Capstone_Project-success" alt="KAU">
        <img src="https://img.shields.io/badge/Audit_Score-80%2F100-green" alt="Audit Score">
        <img src="https://img.shields.io/badge/Invoice_Match-96.6%25-green" alt="Invoice Match">
    </div>

    <hr>

    <h2>📌 Overview</h2>
    <p><strong>AuditAI</strong> is an intelligent AI-powered external auditing system developed as a Senior Capstone Project (CPCS499) at King Abdulaziz University. The system automates financial reconciliation and anomaly detection — replacing time-consuming manual audit procedures with an efficient, scalable, and accurate automated pipeline.</p>
    <p>The system accepts <strong>10 standard financial files</strong> and performs comprehensive validation across <strong>4 audit modules</strong>, tested on real enterprise data.</p>

    <hr>

    <h2>📊 Key Results</h2>
    <table>
        <thead>
            <tr>
                <th>Metric</th>
                <th>Result</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><strong>Overall Audit Score</strong></td>
                <td><strong>80 / 100 (MEDIUM risk)</strong></td>
            </tr>
            <tr>
                <td><strong>Invoice Match Rate</strong></td>
                <td><strong>96.6%</strong> (423/438 invoices)</td>
            </tr>
            <tr>
                <td><strong>VAT Errors Detected</strong></td>
                <td><strong>0</strong> across 436 invoices</td>
            </tr>
            <tr>
                <td><strong>Duplicate Invoices</strong></td>
                <td><strong>0</strong> detected</td>
            </tr>
            <tr>
                <td><strong>Missing Invoice Sequences</strong></td>
                <td><strong>0</strong> gaps found</td>
            </tr>
            <tr>
                <td><strong>AR Reconciliation</strong></td>
                <td><strong>83.8%</strong> (31/37 customers)</td>
            </tr>
            <tr>
                <td><strong>Processing Time</strong></td>
                <td><strong>18–32 minutes</strong> (~4.9 sec/invoice)</td>
            </tr>
            <tr>
                <td><strong>System Completion</strong></td>
                <td><strong>98%</strong> of planned requirements</td>
            </tr>
        </tbody>
    </table>

    <hr>

    <h2>🏗️ System Architecture</h2>
    <pre><code>Excel Files (8) + PDF Invoices (500+)
       ↓
Data Cleaning & Column Mapping
(Smart Column Detector — Arabic & English)
       ↓
Audit Engine
       ↓
┌────────────────────────────────────────────────────────┐
│ Module 1: Sales Invoice Audit   → VAT validation, sequence gaps, duplicates
│ Module 2: Purchases Audit       → Same validation for purchase orders
│ Module 3: AR Reconciliation     → AR_Open + Sales - Receipts = AR_Close
│ Module 4: AP Reconciliation     → AP_Open + Purchases - Payments = AP_Close
│ Module 5: Hybrid PDF Validation → pdfplumber (94.7%) + OCR fallback (5.3%)
└────────────────────────────────────────────────────────┘
       ↓
Risk Scoring System (0–100)
       ↓
Interactive Dashboard + Excel Reports</code></pre>

    <hr>

    <h2>⚙️ Tech Stack</h2>
    <table>
        <thead>
            <tr>
                <th>Technology</th>
                <th>Purpose</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><strong>Python 3.10</strong></td>
                <td>Core programming language</td>
            </tr>
            <tr>
                <td><strong>Pandas</strong></td>
                <td>Financial data processing & reconciliation</td>
            </tr>
            <tr>
                <td><strong>NumPy</strong></td>
                <td>Numerical computations</td>
            </tr>
            <tr>
                <td><strong>pdfplumber</strong></td>
                <td>Digital PDF text extraction (primary)</td>
            </tr>
            <tr>
                <td><strong>Tesseract OCR</strong></td>
                <td>Scanned invoice extraction (fallback)</td>
            </tr>
            <tr>
                <td><strong>OpenCV</strong></td>
                <td>Image preprocessing for OCR accuracy</td>
            </tr>
            <tr>
                <td><strong>pdf2image</strong></td>
                <td>PDF-to-image conversion for OCR pipeline</td>
            </tr>
            <tr>
                <td><strong>Supabase</strong></td>
                <td>Authentication, database & backend</td>
            </tr>
            <tr>
                <td><strong>JavaScript / HTML</strong></td>
                <td>Interactive web dashboard</td>
            </tr>
            <tr>
                <td><strong>Tailwind CSS</strong></td>
                <td>Frontend UI styling</td>
            </tr>
            <tr>
                <td><strong>Google Colab</strong></td>
                <td>Development & testing environment</td>
            </tr>
        </tbody>
    </table>

    <hr>

    <h2>🔍 Audit Modules</h2>

    <h3>Module 1 — Sales Invoice Audit</h3>
    <ul>
        <li>VAT validation: <code>TotalBeforeVAT × 0.15 = VAT</code></li>
        <li>Invoice sequence gap detection</li>
        <li>Duplicate invoice detection</li>
        <li>Total consistency checks</li>
        <li><strong>Result: 0 errors across 436 invoices</strong></li>
    </ul>

    <h3>Module 2 — Purchases Audit</h3>
    <ul>
        <li>Same validation logic applied to purchase orders</li>
        <li><strong>Result: 0 errors detected</strong></li>
    </ul>

    <h3>Module 3 — AR Reconciliation</h3>
    <pre><code>ExpectedClosing = OpeningAR + Sales - Receipts</code></pre>
    <ul>
        <li>37 customers analyzed</li>
        <li>6 exceptions detected (total gap: 56,445 SAR)</li>
        <li>5 exception categories: AR Mismatch, Sales Not Reflected, Receipts without Sales, Possible Advance Receipts, Balanced</li>
    </ul>

    <h3>Module 4 — AP Reconciliation</h3>
    <pre><code>ExpectedClosing = OpeningAP + Purchases - Payments</code></pre>
    <ul>
        <li>12 suppliers analyzed</li>
        <li>8 exceptions detected (data completeness issue in source)</li>
    </ul>

    <h3>Module 5 — Hybrid PDF Validation</h3>
    <table>
        <thead>
            <tr>
                <th>Method</th>
                <th>Invoices</th>
                <th>Percentage</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><strong>pdfplumber (Primary)</strong></td>
                <td>415</td>
                <td>94.7%</td>
            </tr>
            <tr>
                <td><strong>Tesseract OCR (Fallback)</strong></td>
                <td>23</td>
                <td>5.3%</td>
            </tr>
            <tr>
                <td><strong>Total Processed</strong></td>
                <td><strong>438</strong></td>
                <td><strong>100%</strong></td>
            </tr>
        </tbody>
    </table>
    <p><strong>Match Results:</strong></p>
    <ul>
        <li>Full Match: 24 invoices</li>
        <li>Derived Match: 399 invoices</li>
        <li>Partial Match: 15 invoices</li>
        <li>Errors: 0</li>
    </ul>

    <hr>

    <h2>🎯 Risk Classification System</h2>
    <table>
        <thead>
            <tr>
                <th>Score</th>
                <th>Risk Level</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>85–100</td>
                <td>🟢 LOW</td>
                <td>Minimal issues, data reliable</td>
            </tr>
            <tr>
                <td>65–84</td>
                <td>🟡 MEDIUM</td>
                <td>Some discrepancies, review required</td>
            </tr>
            <tr>
                <td>40–64</td>
                <td>🔴 HIGH</td>
                <td>Significant issues, immediate attention</td>
            </tr>
            <tr>
                <td>0–39</td>
                <td>⛔ CRITICAL</td>
                <td>Major failures, data unreliable</td>
            </tr>
        </tbody>
    </table>
    <p><strong>This company's result: 80/100 — MEDIUM</strong></p>

    <hr>

    <h2>💻 Web Application Features</h2>
    <ul>
        <li><strong>Authentication</strong> — Email/password & Google OAuth via Supabase</li>
        <li><strong>Client Management</strong> — Add, manage, and monitor multiple companies</li>
        <li><strong>Audit Periods</strong> — Multiple fiscal years per client</li>
        <li><strong>Document Upload</strong> — 10 file types with validation</li>
        <li><strong>Live Dashboard</strong> — Real-time KPIs, charts, exception tables</li>
        <li><strong>Dark/Light Mode</strong> — Full UI theme support</li>
    </ul>

    <hr>

    <h2>🧠 Key Engineering Decisions</h2>
    <p><strong>Why Hybrid OCR?</strong> Not all invoices are digital PDFs. <code>pdfplumber</code> handles text-based PDFs directly (faster, more accurate), while Tesseract OCR serves as a fallback for scanned invoices — giving the system flexibility across real-world document formats.</p>
    <p><strong>Why Column Mapping instead of NLP?</strong> Financial data is structured — fixed fields, numbers, VAT amounts. Rule-based column mapping with Arabic & English alias dictionaries is faster, more accurate, and easier to maintain than NLP for this domain.</p>
    <p><strong>Why Tolerance in Matching?</strong> Accounting systems introduce floating-point rounding differences. A tolerance of ±1.0 SAR prevents false positives while maintaining audit accuracy.</p>

    <hr>

    <h2>👥 Team</h2>
    <table>
        <thead>
            <tr>
                <th>ID</th>
                <th>Name</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>2244530</td>
                <td>Madyan Mohammed Alammari</td>
            </tr>
            <tr>
                <td>2245434</td>
                <td>Yahya Salah Alwathi</td>
            </tr>
            <tr>
                <td>2244524</td>
                <td>Khaled Salem Tayeb</td>
            </tr>
        </tbody>
    </table>
    <p>
        <strong>Supervisor:</strong> Dr. Asaad Ahmed<br>
        <strong>Course:</strong> CPCS499 — Senior Project<br>
        <strong>Institution:</strong> King Abdulaziz University, Faculty of Computing & Information Technology<br>
        <strong>Submission:</strong> May 2026
    </p>

    <hr>

    <h2>🔐 Note on Source Code</h2>
    <p>Source code is <strong>proprietary</strong> due to use of real enterprise financial data from a client company. The full system is available for <strong>live demonstration upon request</strong>.</p>
    <p>Architecture documentation and the final academic report are available in this repository.</p>

    <hr>

    <h2>🚀 Future Work</h2>
    <ul>
        <li>Integration of Isolation Forest / Autoencoder for unsupervised anomaly detection</li>
        <li>Cloud integration with SAP, Oracle Financials, Zoho Books</li>
        <li>NLP-based intelligent audit recommendations</li>
        <li>Automated PDF report generation (ISA/IFRS format)</li>
        <li>Extended GCC language support for column detection</li>
    </ul>

    <hr>
    <p><em>Built with purpose. Developed at King Abdulaziz University — 2026.</em></p>

</body>
</html>
