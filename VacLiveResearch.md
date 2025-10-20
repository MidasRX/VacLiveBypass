# 🛡️ Vac Live Anti-Cheat: An Overview of Detection Mechanics

This document provides a summary of the observed behavior and detection mechanics of the "Vac Live" anti-cheat system. Please note that this information is based on community observation and analysis.

## Core Philosophy

Vac Live appears to operate on a tiered system, distinguishing between game modes and the blatancy of cheats. Its goal is to balance thorough analysis with rapid responses to obvious offenders.

---

## 💣 Standard Competitive Matches

In a standard 5v5 competitive setting, the system uses a specific "window" for its most intensive analysis, supplemented by an always-on detection for known software.

### 🚨 Tier 1: Immediate Signature-Based Detection

This is the system's first line of defense, active from the very beginning of a match.

* **Target:** Outdated or publicly detected cheat software (e.g., old versions of "Aimware").
* **Mechanism:** The system scans for known software signatures. If a recognized cheat is detected, the ban is swift and decisive.
* **Timeline:** Bans can be issued as early as **Round 2**. This layer acts as a filter for low-effort cheating.

### ⏱️ Tier 2: The Main Analysis Window

For cheats that are not immediately recognized by signature, Vac Live performs a more in-depth behavioral analysis during a specific phase of the game.

* **Activation:** The primary analysis seems to begin at the start of **Round 8**.
* **Conclusion:** The analysis phase concludes at the end of **Round 14**.
* **Mechanism:** During this window, the system is believed to be actively collecting data and analyzing player behavior for anomalies that suggest cheating (unnatural aim, tracking through walls, etc.). If a player is "raging" (cheating blatantly) before this window, their data is likely prioritized for immediate review once the window opens.

---

## 🕊️ Wingman Mode: A Different Approach

The detection logic in Wingman operates on a different timeline and with a more focused scope, likely due to the shorter match length and different pace.

* **Detection Timing:** Analysis and ban waves primarily occur **at the conclusion of the match**, rather than during a mid-game window.
* **Detection Scope:** The system seems to target only the most egregious and obvious forms of cheating. Subtle aim assistance may go unflagged, while blatant cheats are prioritized.

#### Examples of features targeted in Wingman:
* `No Spread` / `Perfect Accuracy`
* `Spinbot`
* Other highly conspicuous features that leave no room for doubt.

---

## 📊 Summary of Detection Logic

| Feature                | Standard Competitive              | Wingman                           |
| :--------------------- | :-------------------------------- | :-------------------------------- |
| **Main Analysis Window** | `Round 8` to `Round 14`           | At the `end of the match`           |
| **Known Cheat Ban** | Very fast (as early as `Round 2`) | Less common; focus is on end-game |
| **Detection Focus** | Broad analysis (subtle to blatant) | Highly blatant cheating only      |

## 📝 Conclusion

In summary, Vac Live is a multi-faceted system that adapts its strategy based on the context. It uses a rapid-response method to eliminate users of known cheats and reserves a specific mid-game window for a deeper, more nuanced analysis in competitive play. In contrast, its Wingman implementation prioritizes catching unambiguous cheaters at the end of the match to maintain game integrity without the need for real-time, intensive analysis.
