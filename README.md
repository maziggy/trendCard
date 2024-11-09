* Trend Card

A custom Lovelace card for displaying calculated metrics trends.

First try writing a custom card. I know it's not perfect. Any contributions, recommendations and comments are welcome!

** Screenshot 

![Screnshot](https://raw.githubusercontent.com/maziggy/trendCard/refs/heads/main/screenshots/screenshot.png)

** Installation

*** Via HACS

1. Ensure you have [HACS](https://hacs.xyz/) installed.
2. In Home Assistant, go to **HACS** > **Frontend**.
3. Click the **"+"** button to add a new repository.
4. Enter the repository URL: `https://github.com/maziggy/trendCard.git`.
5. Select **Dashboard** as the category and **Save**.
6. Once installed, add the card to your Lovelace dashboard.

or simply

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=%40maziggy&repository=https%3A%2F%2Fgithub.com%2Fmaziggy%2FtrendCard%2F&category=Dashboard)

** Configuration

```yaml
type: custom:trend-card
interval: input_number.trend_interval
steps: input_number.trend_values
interval_remaining: input_text._trend_interval_remaining
metric1_delta: sensor.temperature_last
metric1_name: Temp
metric2_delta: sensor.humidity_last
metric2_name: Hum
metric3_delta: sensor.water_last
metric3_name: WAT
refresh: 60

I have a Python script that feeds the required sensors. Unfortunately this is not yet ready for publishing. I'll work on this the next time.

As long as i didn't published the data calculation script, PLEASE NOTE:

input_text._trend_interval_remaining must be a input_text.sensor with state "<current_counter/steps>" - for example "2/6". Of course without the quotation marks ;)

