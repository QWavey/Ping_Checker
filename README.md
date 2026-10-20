# Ping_Checker

An interactive Python tool that sends HTTP requests to a URL while it varies speed, growth, payload size, stacking, and delay. Use it to find out when a website starts denying requests.

It runs in **easy mode** (guided prompts) or **advanced mode** (72 predefined test types).

## Features

- **Interactive test runner:** sends HTTP requests with configurable parameters.
- **Two modes:**
  - **Easy:** guided prompts for speed, growth, size change, stacking, and delay.
  - **Advanced:** pick one of the 72 predefined test types.
- **Color-coded output:** ANSI colors highlight speed, growth, size, and delay.
- **Live output:** prints each response with its elapsed time, packet size, and progress.
- **Stops on failure:** the run ends when requests fail or are denied.

## Parameters

The tool varies these attributes:

| Parameter | Options | Description |
| --- | --- | --- |
| **Speed** | `slow`, `fast`, `variable` | Sets how often pings are sent |
| **Growth** | `slow`, `rapid` | Sets how fast the payload grows |
| **Size** | `bigger`, `same` | Whether the payload size changes |
| **Stacking** | `yes`, `no` | Sends several stacked pings per iteration (still in testing) |
| **Delay** | `none`, `fixed`, `dynamic` | Adds an artificial delay between requests |

Combined, these give **72 unique test types**.

## Installation

```bash
git clone https://github.com/XQuantumWaveX/Ping_Checker/
cd Ping_Checker
pip install requests
```

## Usage

```bash
python Ping_Test.py --url https://example.com --max_requests 50
```

The tool then asks you to choose easy mode or advanced mode.

### Easy mode

```
Select mode (easy / advanced): easy
Choose Speed (Options: slow, fast, variable): fast
Choose Growth (Options: slow, rapid): rapid
Choose Size Change (Options: bigger, same): bigger
Choose Stacking (Options: no, yes): yes
Choose Delay (Options: none, fixed, dynamic): dynamic
```

### Advanced mode

Advanced mode lists all 72 predefined test types in a table:

```
Select mode (easy / advanced): advanced
Select a test type (1-72):
+-----+----------+--------+-------------+----------+---------+
| Num | Speed    | Growth | Size Change | Stacking | Delay   |
+-----+----------+--------+-------------+----------+---------+
| 1   | slow     | slow   | bigger      | no       | none    |
| 2   | slow     | slow   | bigger      | no       | fixed   |
...
Enter test type number (1-72): 15
```

## Example output

```
=== Running Test ===
Speed: fast, Growth Rate: rapid, Size Change: bigger, Stacking: yes, Delay: dynamic

Ping 3-2: status=200, time=0.045s, size=144B, Speed: fast, Pings received: 10
```

## Notes

- Use it against test or staging environments. Depending on the settings, it can generate heavy request loads.
- Don't run it against production systems without permission.
- The output depends on your network speed and CPU speed.
- I am not responsible for damage this script causes. Whoever runs it is responsible for their own actions.

## Planned

- An option to hold a specific byte size, for tests that need an exact payload size.
