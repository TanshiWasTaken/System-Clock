# System Clock

A small Nintendo Switch homebrew overlay for changing the system clock from Ultrahand.

It uses a privileged sysmodule to apply the clock changes.

## Features

- Change the year, month, day, hour, minute, and second
- Apply a custom time
- Reload the current system time
- Reset the clock to real time

## Requirements

- Nintendo Switch
- Atmosphère
- Hekate
- Ultrahand

Tested on:

- HOS 22.5.0
- Atmosphère 1.11.2
- Hekate: 6.5.3

Other versions may work, but haven't been tested.

## Installation

Copy the sysmodule to your SD card:

```text
sd:/atmosphere/
├── contents/
│   └── 4200000000000C10/
│       ├── toolbox.json
│       ├── exefs.nsp
│       └── flags/
│           └── boot2.flag
└── ...
```

Copy the overlay to:

```text
sd:/switch/
├── .overlays/
│   └── system-clock.ovl
└── ...
```

Reboot the Switch after installing the sysmodule.

It is recommended you check using [Hekate Toolbox](https://github.com/WerWolv/Hekate-Toolbox/releases) that the `sys-edit-time` sysmodule loaded and correctly shows "On" in the "Background services" menu.

Open Ultrahand and launch System Clock.

## If it doesn't work

If the overlay doesn't appear:

- Make sure `system-clock.ovl` is in `sd:/switch/.overlays/`
- Make sure Ultrahand is running
- Reboot after installing the sysmodule

If the overlay opens but changes don't apply:

- Make sure the sysmodule is installed correctly
- Check that `boot2.flag` exists and that it is running (shows "On") using Hekate Toolbox
- Toggle the sysmodule off then back on again from inside Hekate Toolbox
- Reboot the Switch
- Check the Atmosphère logs, if available

If you still can't get it working, open an issue with:

- HOS version
- Atmosphère version
- Hekate version
- Reproduction steps
- Any relevant error messages and screenshots

## Credits

Built using libnx, libtesla/libultrahand, and Atmosphère/stratosphere.

## License

Closed-source
