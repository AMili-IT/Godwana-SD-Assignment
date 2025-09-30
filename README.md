````markdown
# Godwana-SD-Assignment

This project is a simple web-based tool to check unit availability and rates.  
It uses a **PHP backend** (`api.php`) and a **HTML/JS frontend** (`index.html`).  
The project also integrates with **SonarCloud** for code quality checks.

---

## 📂 Files in this Repository

- **`index.html`** – Frontend user interface. Users enter unit name, dates, occupants, and ages, then click **Check** to fetch rates.
- **`api.php`** – Backend script. Accepts JSON payload from the frontend and communicates with the external Gondwana API to fetch rates and availability.
- **`devcontainer.json`** – Development container configuration (for GitHub Codespaces or VS Code Remote Containers).
- **`sonarcloud.yml`** – SonarCloud pipeline configuration for static code analysis and quality checks.

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd <repo-folder>
````

2. Start a local PHP server:

   ```bash
   php -S localhost:8000
   ```

3. Open the frontend in your browser:

   ```
   http://localhost:8000/index.html
   ```

---

## 🖥️ How It Works

1. The user fills in:

   * **Unit Name** (e.g. "Luxury Unit")
   * **Arrival** and **Departure** dates (dd/mm/yyyy format)
   * **Number of Occupants**
   * **Ages** (comma-separated list, e.g. `30,10`)

2. When the **Check** button is clicked:

   * The frontend sends a JSON payload to `api.php`.
   * `api.php` processes the request and calls the Gondwana API.
   * The response (Rate, Availability, Date Range) is displayed below the form.

---

## ✅ Example Payload Sent to `api.php`

```json
{
  "Unit Name": "Luxury Unit",
  "Arrival": "26/09/2025",
  "Departure": "28/11/2025",
  "Occupants": 2,
  "Ages": [30, 10]
}
```

---

## 📊 SonarCloud

This repository includes a **SonarCloud integration** via `sonarcloud.yml`.
It runs code quality checks automatically on commits and pull requests.

---

## 📝 Notes

* Ensure your PHP environment is running before testing.
* The external Gondwana API must be accessible for rate/availability results.
* If the API is unreachable, `Rate` and `Availability` will display as `N/A`.

---

```
```
