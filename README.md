# India-Stocks-2251-2280-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2251 to 2280)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2251-2280-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2251 to 2280)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2251 | `SONAL` | Sonal Mercantile Limited | `SONAL.NS` |
| 2252 | `SONAMLTD` | SONAM LIMITED | `SONAMLTD.NS` |
| 2253 | `SONATSOFTW` | Sonata Software Limited | `SONATSOFTW.NS` |
| 2254 | `SOTL` | Savita Oil Technologies Limited | `SOTL.NS` |
| 2255 | `SOUTHBANK` | The South Indian Bank Limited | `SOUTHBANK.NS` |
| 2256 | `SOUTHWEST` | South West Pinnacle Exploration Limited | `SOUTHWEST.NS` |
| 2257 | `SPAL` | S. P. Apparels Limited | `SPAL.NS` |
| 2258 | `SPANDANA` | Spandana Sphoorty Financial Limited | `SPANDANA.NS` |
| 2259 | `SPARC` | Sun Pharma Advanced Research Company Limited | `SPARC.NS` |
| 2260 | `SPCENET` | Spacenet Enterprises India Limited | `SPCENET.NS` |
| 2261 | `SPECIALITY` | Speciality Restaurants Limited | `SPECIALITY.NS` |
| 2262 | `SPECTRUM` | Spectrum Electrical Industries Limited | `SPECTRUM.NS` |
| 2263 | `SPENCERS` | Spencer's Retail Limited | `SPENCERS.NS` |
| 2264 | `SPIC` | Southern Petrochemicals Industries Corporation  Limited | `SPIC.NS` |
| 2265 | `SPLIL` | SPL Industries Limited | `SPLIL.NS` |
| 2266 | `SPLPETRO` | Supreme Petrochem Limited | `SPLPETRO.NS` |
| 2267 | `SPMLINFRA` | SPML Infra Limited | `SPMLINFRA.NS` |
| 2268 | `SPORTKING` | Sportking India Limited | `SPORTKING.NS` |
| 2269 | `SRD` | Shankar Lal Rampal Dye-Chem Limited | `SRD.NS` |
| 2270 | `SREEL` | Sreeleathers Limited | `SREEL.NS` |
| 2271 | `SRGHFL` | SRG Housing Finance Limited | `SRGHFL.NS` |
| 2272 | `SRHHYPOLTD` | Sree Rayalaseema Hi-Strength Hypo Limited | `SRHHYPOLTD.NS` |
| 2273 | `SRIKPRIND` | Sri KPR Industries Limited | `SRIKPRIND.NS` |
| 2274 | `SRIT` | SRIT India Limited | `SRIT.NS` |
| 2275 | `SRM` | SRM Contractors Limited | `SRM.NS` |
| 2276 | `SRTL` | Shree Ram Twistex Limited | `SRTL.NS` |
| 2277 | `SSDL` | Saraswati Saree Depot Limited | `SSDL.NS` |
| 2278 | `SSRETAIL` | SS Retail Limited | `SSRETAIL.NS` |
| 2279 | `SSWL` | Steel Strips Wheels Limited | `SSWL.NS` |
| 2280 | `STALLION` | Stallion India Fluorochemicals Limited | `STALLION.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream SONAL 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2251-2280-Historical-Data/main/SONAL/1m/2026/10/SONAL_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
