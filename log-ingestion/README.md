# 📥 Log Ingestion & Validation – Splunk SIEM

---

## 📌 Objective

The objective of this phase is to ingest Linux authentication logs into Splunk SIEM to enable **centralized log analysis, security monitoring, and detection engineering**.

This establishes a reliable data pipeline required for **threat detection and incident investigation**.

---

## 🔎 Log Source

The primary log source onboarded:

```bash
/var/log/auth.log
```

This log contains:

* Successful and failed authentication attempts
* Privilege escalation activity (sudo)
* User session events
* System-level authentication logs

---

## 🛠️ Implementation Steps

### Step 1: Verify Log Availability

Confirm that authentication logs are being generated:

```bash
sudo tail -f /var/log/auth.log
```

This ensures real-time log activity before ingestion.

📸 **Output verification:**

![Data Input](../log-ingestion/screenshots/4_log_ingestion.png)
---

### Step 2: Configure File Permissions

Grant Splunk access to the log file:

```bash
sudo chmod 644 /var/log/auth.log
sudo chown splunk:splunk /var/log/auth.log
```

This allows the Splunk service to read the log file.

📸 **Permission configuration:**

![Permissions](screenshots/2_data_input_config.png)

---

### Step 3: Restart Splunk Service

Apply permission changes by restarting Splunk:

```bash
/opt/splunk/bin/splunk restart
```

---

### Step 4: Configure Data Input (Splunk Web)

1. Navigate to: **Settings → Add Data**
2. Select: **Monitor**
3. Choose: **Files & Directories**
4. Enter the log path:

```bash
/var/log/auth.log
```

This enables continuous monitoring of the authentication log.

📸 **Splunk data input setup:**

![Data Input](screenshots/2_data_input_config.png)

---

### Step 5: Define Source Type

Set the sourcetype as:

```bash
linux_secure
```

This ensures proper parsing, timestamp recognition, and field extraction.

---

### Step 6: Validate Data Ingestion

Run the following SPL query:

```bash
index=main source="/var/log/auth.log"
```
📸 **Search result in splunk:**

![Validation](./screenshots/5_attack_simulation.png)


---

## 📊 Validation Results

* Logs successfully ingested into Splunk
* Events properly parsed using `linux_secure` sourcetype
* Authentication activity visible and searchable
* Environment ready for detection and analysis

---

## ✅ Outcome

* Established a working log ingestion pipeline
* Enabled visibility into authentication events
* Prepared the SIEM environment for detection engineering and threat investigation

---
