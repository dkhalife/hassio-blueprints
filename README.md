# Home Assistant Blueprints

**Automate smarter, live easier!**

A collection of free and open-source Home Assistant automation blueprints designed to cover everyday smart home use cases out of the box. Import any blueprint in one click and get a fully configurable automation without writing a single line of YAML.

## ✨ Blueprints

### 🔌 Device Limiter

> Turns a device off after a configurable amount of time has elapsed since it was turned on.

Useful for devices you frequently forget to turn off (e.g. a bathroom light or a garage fan).

| Input | Description | Default |
|---|---|---|
| `device` | The light or switch to monitor and turn off | — |
| `time` | How long to wait before turning the device off | 1 hour |
| `notify` | Mobile device to notify when the device is turned off | — |
| `message` | Notification message body | `Device has been turned off` |

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fdkhalife%2Fhassio-blueprints%2Fmain%2Fdevice_limiter.yaml)

---

### 🔒 Lock Notifications

> Sends a notification whenever a lock is unlocked, and a follow-up notification if it stays unlocked for too long.

Two triggers are handled: the moment the lock is unlocked, and again after a configurable duration if it has not been re-locked.

| Input | Description | Default |
|---|---|---|
| `lock` | The lock entity to monitor | — |
| `notify` | Mobile device to send notifications to | — |
| `message_just_unlocked` | Message sent as soon as the lock is unlocked | `Unlocked` |
| `time` | Duration before assuming the lock was left unlocked | 5 minutes |
| `message_left_unlocked` | Message sent if the lock remains unlocked | `Left unlocked` |

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fdkhalife%2Fhassio-blueprints%2Fmain%2Flock_notifications.yaml)

---

### 💡 Light Switch Synchronization

> Keeps one or more lights in sync with a switch entity.

When the switch turns on, all linked lights turn on — and vice versa. Useful when a switch entity is not natively bound to physical lights.

| Input | Description |
|---|---|
| `switch` | The switch that controls the lights |
| `lights` | One or more light entities to keep in sync |

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fdkhalife%2Fhassio-blueprints%2Fmain%2Fsynchronize_lights_to_switch.yaml)

---

### ⏰ Timed Lights

> Turns lights (or switches) on at a scheduled time and off at another, with optional notifications.

| Input | Description | Default |
|---|---|---|
| `lights` | The lights or switches to control | — |
| `start_time` | Time to turn the lights on | 17:10 |
| `end_time` | Time to turn the lights off | 18:00 |
| `notify` | Mobile device for turn-on/off notifications | — |
| `message_on` | Message sent when lights turn on | `Lights turned on automatically` |
| `message_off` | Message sent when lights turn off | `Lights turned off automatically` |

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fdkhalife%2Fhassio-blueprints%2Fmain%2Ftimed_lights.yaml)

---

### ✅ ToDo — Clear Completed

> Automatically deletes completed items from one or more ToDo lists at a scheduled time each day.

| Input | Description | Default |
|---|---|---|
| `lists` | The ToDo list entities to clean up | — |
| `notification_time` | Time at which to perform the cleanup | 08:00 |

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fdkhalife%2Fhassio-blueprints%2Fmain%2Ftodo_clear_completed.yaml)

---

### 📅 ToDo — Due Reminders

> Sends a daily notification listing all tasks that are due today across one or more ToDo lists.

| Input | Description | Default |
|---|---|---|
| `lists` | The ToDo list entities to scan | — |
| `notification_time` | Time at which to send the notification | 08:00 |
| `notify` | Mobile device to receive the notification | — |

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fdkhalife%2Fhassio-blueprints%2Fmain%2Ftodo_due_notifications.yaml)

---

### ⚠️ ToDo — Overdue Reminders

> Sends a daily notification listing all tasks whose due date has already passed across one or more ToDo lists.

| Input | Description | Default |
|---|---|---|
| `lists` | The ToDo list entities to scan | — |
| `notification_time` | Time at which to send the notification | 08:00 |
| `notify` | Mobile device to receive the notification | — |

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fdkhalife%2Fhassio-blueprints%2Fmain%2Ftodo_overdue_notifications.yaml)

---

## 🚀 Installation

Each blueprint has an **Import blueprint** button above that opens Home Assistant directly. You can also import manually:

1. Go to **Settings → Automations & Scenes → Blueprints**
2. Click **Import Blueprint** in the bottom-right corner
3. Paste the raw URL of any `.yaml` file from this repository
4. Click **Preview** and then **Import**

Once imported, create automations from the blueprint by clicking **Create automation** and filling in the inputs.

## 🤝 Contributing

Contributions are welcome! If you have an idea for a new blueprint or an improvement to an existing one, feel free to fork the repo and submit a pull request. If you have ideas but aren't familiar with YAML or Home Assistant automations, you can [open an issue](https://github.com/dkhalife/hassio-blueprints/issues) instead.

## 🔒 License

See the [LICENSE](LICENSE) file for more details.
