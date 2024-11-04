# trendChart

A custom dashboard card for displaying calculated metrics trends.

First try writing a custom card. I know it's not perfect. Any contributions, recommendations and comments are welcome!

## Installation

### Via HACS

1. Ensure you have [HACS](https://hacs.xyz/) installed.
2. In Home Assistant, go to **HACS** > **Frontend**.
3. Click the **"+"** button to add a new repository.
4. Enter the repository URL: `https://github.com/maziggy/trend[BChart.git`.
5. Select **Dashboard** as the category and **Save**.
6. Once installed, add the card to your Lovelace dashboard.

or simply

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Martin+Ziegler&repository=https%3A%2F%2Fgithub.com%2Fmaziggy%2FppfdChart.git&category=Dashboard)

## Configuration

```yaml
type: custom:growbox-trend-card
interval: input_number.growbox_trend_interval
steps: input_number.growbox_trend_values
interval_remaining: input_text.growbox_trend_interval_remaining
temperature_delta: sensor.growbox_temperature_last
humidity_delta: sensor.growbox_humidity_last
vpd_delta: sensor.growbox_vpd_last
refresh: 60
