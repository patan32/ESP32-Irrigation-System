Change your weather entity name from HA for weather to work properly. Look for weather.forecast_home entity and change it to what you have in HA for weather. 

🌱 Core System Enhancements

Hunter Pro-C–style controller logic implemented

8 zones supported, each independently configurable

Optional Master Valve with per-zone enable/disable

Station delay between zones (default 5s)

📅 Scheduling & Programs

3 Programs (A, B, C)
Each program supports:

Enable/disable

Start time (12-hour format with AM/PM)

Schedule types:

Specific days

Odd days

Even days

Interval (every X days)

Zones can be assigned to any program

Individual zone schedules (zones can run standalone, outside programs)

⏱️ Queue & Run Control (Big Upgrade)

3-slot run queue (Hunter-style)

Programs and manual runs queue instead of failing

Prevents overlapping starts

Run lock (irrigation_busy) to avoid double execution

Auto-advance between queued runs

Safe stop → restart cooldown to prevent relay thrashing

⏸️ Pause / Resume (Proper Implementation)

True Pause & Resume support:

Remembers active zone

Remembers remaining time

Preserves cycle/soak state

Resumes exactly where it left off

Handles pause during watering OR soaking

💧 Cycle & Soak (Smart Watering)

Global Cycle & Soak mode

Configurable:

Cycle duration

Soak duration

Tracks:

Total cycles

Elapsed time

Active soak vs watering phase

🌦️ Weather & Rain Intelligence

Automatic rain delay based on HA weather entity

Delays irrigation during:

Rain

Pouring

Snow / snowy-rain

Manual overrides:

Rain delay override

Weather override (force watering)

Weather checks run every 4 hours

⏰ Time Restrictions

Configurable watering blackout window

12-hour time + AM/PM

Blocks:

Programs

Zone schedules

Logs restriction warnings only once per hour (spam-safe)

🌡️ Smart Seasonal Multiplier

Automatic water multiplier based on:

Season (month)

Outdoor temperature

Examples:

Summer + hot → up to 1.8×

Winter + cold → as low as 0.3×

Applied:

On boot

Retry if HA time isn’t ready

Every midnight

Manual “normal” multiplier preserved

🧠 State Tracking & Persistence

Remembers across reboot:

Rain delay

Program settings

Zone schedules

Master valve settings

Tracks:

Last watered time per zone

Zone start timestamps

Program last-run timestamps

🖥️ Diagnostics & UX

Clear valve status text sensor

Structured, readable log output

Spam-reduced warnings (weather & time restriction)

Web server enabled for quick access

API + OTA secured
