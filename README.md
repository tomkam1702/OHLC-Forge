<p align="center">
  <img src="images/OHLC_Forge_Logo.png" width="400" alt="OHLC Forge Logo">
</p>

# OHLC Forge
### Professional OHLC Daily Data Reconstruction for Crypto Traders

Build your own historical OHLC daily data database for Binance and Bybit perpetual markets with **custom session close times**. No more midnight alarms – trade on your own schedule.

> [!NOTE]
> **⏰ How Custom Session Timing Works**
> By selecting the correct offset, you force the daily bar to close during your comfortable local evening, rather than at midnight UTC. This allows you to download data and run your trading system at a normal hour. For example, the bar labelled **`2025-12-02`** covers:
> 
> | Setting | 24-Hour Period (UTC) | 24-Hour Period (Local Time) |
> | :--- | :--- | :--- |
> | **UTC+4** | `1 Dec 20:00` →<br>`2 Dec 20:00 (UTC)` | `1 Dec 21:00` →<br>`2 Dec 21:00 (Berlin, CET)` |
> | **UTC+11** | `1 Dec 13:00` →<br>`2 Dec 13:00 (UTC)` | `1 Dec 22:00` →<br>`2 Dec 22:00 (Tokyo, JST)` |
> | **UTC+13** | `1 Dec 11:00` →<br>`2 Dec 11:00 (UTC)` | `1 Dec 22:00` →<br>`2 Dec 22:00 (Sydney)` |

---

## ⚡ Quick Navigation

<table>
  <tr>
    <td align="center"><a href="https://github.com/tomkam1702/OHLC-Forge/releases">🚀 Download OHLC Forge PRO</a></td>
    <td align="center"><a href="https://github.com/tomkam1702/OHLC-Forge/releases">🎁 Download OHLC Forge FREE (Demo)</a></td>
    <td align="center"><a href="https://tomkam1702.github.io/OHLC-Forge/user_guide.html">📖 Full User Guide (Online)</a></td>
  </tr>
  <tr>
    <td colspan="3" align="center">
      <strong><a href="https://gumroad.com/l/ohlc-forge">💎 Get OHLC Forge PRO licence (Gumroad)</a></strong>
    </td>
  </tr>
</table>

---

## 📊 Free vs PRO Comparison

Experience the power of custom time zones. Start with the Free Demo and upgrade when you're ready for the full market.

| Feature | OHLC Forge FREE (Demo) | OHLC Forge PRO |
| :--- | :--- | :--- |
| **Exchanges** | Binance, Bybit | **Binance, Bybit** |
| **Supported Symbols** | BTC/USDT, ETH/USDT | **All (600+) Perpetual Pairs** |
| **Daily Bar Time Zone** | Forced UTC±0 | **40 Options (UTC-20 to UTC+20)** |
| **Reconstruction Method** | Simple 1d Fetch | **Precise 1h Reconstruction** |
| **Operation Modes** | Update, Fill Gaps, Redownload | **Update, Fill Gaps, Redownload** |
| **Multi-threading** | Yes | **Yes (High Performance)** |
| **DPI-Aware UI** | Yes | **Yes** |

---

![OHLC Forge Banner](images/whole_window_new.png)

### Precise Configuration
Choose from **40 different time zone offsets** (from UTC-20 to UTC+20) to perfectly match your local evening routine.

![Configuration](images/configuration_new.png)

### Three Operation Modes
Seamlessly update your database with missing bars, fill historical gaps, or perform a full redownload from a specific date.

![Operation Modes](images/operation_mode.png)

### High-Quality CSV Output
OHLC Forge generates clean, standard CSV files compatible with **AmiBroker, TradingView, Excel, Python (Pandas)**, and any other technical analysis software. All prices are formatted with a fixed number of decimal places, strictly following the market specification (tick size). The application retrieves the official tick size (price precision) from each exchange and formats all prices accordingly.

**📈 High-Price Market (BTC)**  
Bitcoin trades with **1 decimal place** precision:
```text
20251201,90308.6,90374.4,83755.3,86244.1,12214858119
20251202,86244.1,92298.9,86148.4,91241.7,9616542596
20251203,91241.7,94189.4,90945.0,93390.1,9571207300
20251204,93390.1,94058.1,90800.0,92031.8,6933686131
20251205,92031.8,92658.3,88002.1,89273.7,8427872957
```

**💎 Low-Price Market (Meme Coin)**  
Markets like 1000000BABYDOGEUSDT use **7 decimal places**:
```text
20251201,0.0006972,0.0006982,0.0006300,0.0006585,1068182
20251202,0.0006585,0.0007163,0.0006510,0.0007028,859501
20251203,0.0007028,0.0007599,0.0007028,0.0007516,1067822
20251204,0.0007516,0.0007654,0.0007113,0.0007137,573909
20251205,0.0007137,0.0007195,0.0006547,0.0006754,1108743
```

### Professional Update Logs
Monitor your download progress, API rate limits, and network connection status in real-time through a clear, professional text log.

![Update Log](images/update_log.png)

---

## 🎯 The Problem with Default Daily Bars

Most cryptocurrency exchanges close their daily candles at **00:00 UTC**. This is an international standard, but it creates a real problem for systematic traders who need to update their data and place orders every day.

*   🌙 **Default: UTC+0**
    *   **00:00 - 02:00**
    *   Daily bar closes at **midnight UTC**
    *   *For most traders, this means staying up late at night or waking up in the middle of the night to update data and place orders.*

*   ✨ **Custom Time Zone**
    *   **21:00 - 22:00**
    *   Daily bar closes at **your chosen time**
    *   *Update your data, place your orders, and go to bed at a reasonable hour. Same trading system, same logic, better lifestyle.*

---

## 🌍 Real Examples: Traders Around the World

See how the default 00:00 UTC close time affects traders in different locations, and how **OHLC Forge** solves this problem:

### <img src="images/DE.svg" alt="DE" height="20" align="absmiddle"> Hans from Berlin (Germany, CET = UTC+1)
*   **Default UTC+0:** `01:00` (middle of the night)
*   **With OHLC Forge:** `21:00` (relaxed evening)
> *"I was setting alarms for 1 AM every night. Now I update my data at 9 PM and sleep well."*
> **Recommended: UTC+4**

### <img src="images/CN.svg" alt="CN" height="20" align="absmiddle"> Wei from Shanghai (China, CST = UTC+8)
*   **Default UTC+0:** `08:00` (morning rush hour)
*   **With OHLC Forge:** `21:00` (calm evening)
> *"An 8 AM bar close meant rushing before work. Now I trade comfortably after dinner."*
> **Recommended: UTC+11**

### <img src="images/NZ.svg" alt="NZ" height="20" align="absmiddle"> Emma from Auckland (New Zealand, NZDT = UTC+13 in summer)
*   **Default UTC+0:** `13:00` (lunch at work)
*   **With OHLC Forge:** `22:00` (home sweet home)
> *"I couldn't check my system during my lunch break at work. Evening trading changed everything."*
> **Recommended: UTC+15**

### <img src="images/US.svg" alt="US" height="20" align="absmiddle"> Mike from Los Angeles (USA West Coast, PST = UTC-8)
*   **Default UTC+0:** `16:00` (still at work)
*   **With OHLC Forge:** `21:00` (evening at home)
> *"Default close time was during my commute. Now I trade after putting the kids to bed."*
> **Recommended: UTC-5**

---

## 📋 Quick Reference: Time Zone Settings

Find your location and recommended setting for evening (21:00–22:00) data updates:

| Location | Local Offset | Default Close (00:00 UTC) | Problem | Recommended Setting | New Close (Local Time) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| <img src="images/DE.svg" alt="DE" height="20" align="absmiddle"><br>**Berlin** | UTC+1 / +2 | 01:00 / 02:00 | 🌙 Middle of night | **UTC+4** | ✨ 21:00 / 22:00 |
| <img src="images/GB.svg" alt="GB" height="20" align="absmiddle"><br>**London** | UTC+0 / +1 | 00:00 / 01:00 | 🌙 Midnight | **UTC+3** | ✨ 21:00 / 22:00 |
| <img src="images/CN.svg" alt="CN" height="20" align="absmiddle"><br>**Beijing** | UTC+8 | 08:00 | 🏃 Morning rush | **UTC+11** | ✨ 21:00 |
| <img src="images/JP.svg" alt="JP" height="20" align="absmiddle"><br>**Tokyo** | UTC+9 | 09:00 | 💼 Work hours | **UTC+11** | ✨ 22:00 |
| <img src="images/NZ.svg" alt="NZ" height="20" align="absmiddle"><br>**Wellington** | UTC+12 / +13 | 12:00 / 13:00 | 🍽️ lunch break | **UTC+15** | ✨ 21:00 / 22:00 |
| <img src="images/AU.svg" alt="AU" height="20" align="absmiddle"><br>**Sydney** | UTC+10 / +11 | 10:00 / 11:00 | 💼 Work hours | **UTC+13** | ✨ 21:00 / 22:00 |
| <img src="images/US.svg" alt="US" height="20" align="absmiddle"><br>**Los Angeles** | UTC-8 / -7 | 16:00 / 17:00 | 💼 Still at work | **UTC-5** | ✨ 21:00 / 22:00 |
| <img src="images/US.svg" alt="US" height="20" align="absmiddle"><br>**New York** | UTC-5 / -4 | 19:00 / 20:00 | 🍽️ Dinner time | **UTC-2** | ✨ 21:00 / 22:00 |
| <img src="images/BR.svg" alt="BR" height="20" align="absmiddle"><br>**São Paulo** | UTC-3 | 21:00 | ✓ Already good! | **UTC+0** | ✨ 21:00 |

> ⚠️ **Important: UTC Offsets Are Fixed, Your Local Time Changes**
> The time zone settings in OHLC Forge (e.g., UTC+3) are **fixed UTC offsets**, not dynamic time zones that adjust for Daylight Saving Time (DST). The daily bar always closes at exactly the same moment in UTC. However, your local clock time for that moment will shift by 1 hour when your region switches between standard time and daylight saving time.

---

## ❓ Frequently Asked Questions

### Will my trading system perform differently with custom time zone data?
Results should be **very similar**, though minor differences are expected. The underlying price movements are the same — you're just slicing the 24-hour periods at different points. If your backtest results change *significantly* when shifting the daily bar close time by a few hours, this is a strong indicator that your system may be **overfitted (curve-fitted)**.

### Why do exchanges use UTC+0 by default?
UTC is the international standard for timekeeping. It's neutral and doesn't favour any particular region. However, "neutral" for the world often means "inconvenient" for individual traders.

### Can I use multiple time zone settings for the same symbol?
Yes! OHLC Forge creates separate data files for each exchange. You can run the tool multiple times with different settings and save to different folders.

### What about weekends? Crypto trades 24/7.
Correct — crypto markets never close. Your daily bars will be continuous, including Saturday and Sunday. The time zone setting simply determines when each 24-hour period begins and ends.

### How is this different from simply using exchange data?
Exchange data only provides UTC+0 daily bars (closing at midnight UTC). OHLC Forge downloads hourly data and reconstructs daily bars according to your chosen time zone. This is the **only** way to obtain custom time zone daily data for crypto.

---

## ✨ OHLC Forge PRO Features

*   🌐 **40 Time Zones:** From UTC−20 to UTC+20, find the perfect closing time for your schedule.
*   📈 **600+ Pairs:** All perpetual futures from Binance and Bybit in one click.
*   🔧 **3 Modes:** Update, Fill Gaps, or Redownload your data as needed.
*   💾 **CSV Format:** Ready for AmiBroker, TradingView, Excel, Python, and more.
*   ⚡ **Multi-threaded:** Fast parallel downloads — update all pairs in minutes.
*   🖥️ **Easy GUI:** No coding required. Click, configure, download.

---

## 🚀 Ready to Trade on Your Schedule?
Stop staying up late or missing signals. Get daily crypto data that closes when *you* want it to.

### [👉 Get OHLC Forge PRO on Gumroad](https://gumroad.com/l/ohlc-forge)

*One-time purchase • Sold "as is" • 40 time zone options • 600+ crypto pairs*

---

## ⚖️ Legal Disclaimer and Terms of Use

**1. Software Tool Nature:** OHLC Forge PRO ("the Software") is a technical utility designed solely to facilitate the downloading and processing of public market data. The Software is sold strictly as a data processing tool. It does not contain, resell, or distribute any financial market data, historical price data, or exchange feeds.

**2. Third-Party Libraries:** The Software utilises the open-source CCXT library (MIT Licence) to interface with cryptocurrency exchanges. CCXT is an independent project and is not affiliated with OHLC Forge PRO.

**3. User-Initiated Data Access:** All data processed by the Software is downloaded directly by the user from third-party exchanges (e.g., Binance, Bybit) using their public Application Programming Interfaces (APIs). The Software acts merely as an interface to execute these requests on the user's behalf and on the user's local machine.

**4. User Responsibility:** You, the user, acknowledge that you are accessing these APIs directly. It is your sole responsibility to ensure that your use of these APIs, including the frequency and purpose of data requests, complies with the respective Terms of Service, API Usage Policies, and rate limits as published by each exchange. Violations of exchange rate limits may result in temporary or permanent API access restrictions imposed by the exchange, for which the developer bears no responsibility.

**5. No Affiliation:** OHLC Forge PRO is an independent software product and is not affiliated with, endorsed by, sponsored by, or in any way officially connected with Binance, Bybit, CCXT, or any of their subsidiaries or affiliates. "Binance" and "Bybit" are registered trademarks of their respective owners.

**6. No Financial Advice & "As Is" Warranty:** This Software is provided "as is", without warranty of any kind, express or implied. The developer makes no representations or warranties regarding the accuracy, completeness, or reliability of the data fetched by the Software. Nothing in this product or documentation constitutes financial, investment, or trading advice. Past performance of any trading system does not guarantee future results.

**7. LIMITATION OF LIABILITY:** IN NO EVENT SHALL THE DEVELOPER, COPYRIGHT HOLDERS, OR CONTRIBUTORS BE LIABLE FOR ANY INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, CONSEQUENTIAL, OR PUNITIVE DAMAGES, INCLUDING BUT NOT LIMITED TO LOSS OF PROFITS, DATA, OR USE, ARISING OUT OF OR IN CONNECTION WITH THE USE OF THIS SOFTWARE, REGARDLESS OF THE CAUSE OF ACTION OR THE THEORY OF LIABILITY, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.
