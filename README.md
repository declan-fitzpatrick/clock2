# Module: Clock

The `clock` module is one of the default modules of the MagicMirror.
This module displays the current date and time. The information will be updated realtime.

For configuration options, please check the [MagicMirror² documentation](https://docs.magicmirror.builders/modules/clock.html).

## Installation

```
cd modules
git clone https://github.com/declan-fitzpatrick/clock2.git
```

## Usage

```javascript
    {
        module: "clock2",
        position: "middle_center",
        config: {
            displayType: "analog",
            analogFace: "face-003",
            analogSize: "600px",
            displaySeconds: "true",
            timeFormat: "24",
            showPeriod: "false",
            analogShowDate: "false",
            clockBold: "true",
            analogPlacement: "top"
        }
    },
```

## Duplication of the clock module

I have duplicated this clock module so that I can create two instances (an analogue and digital) of it on my Magic mirror [some context](https://forum.magicmirror.builders/topic/12333/adding-duplicate-modules/2), to use with [MMM-Pages](https://github.com/edward-shen/MMM-pages). Changes compared to default clock are:

- `clock.js` renamed to `clock2.js`.
- renamed the module registration in `clock2.js` to `clock2`.

```javascript
...
Module.register("clock2", {
    ...
});
...

```

Did not overwrite `clock_styles.css` or its contents, as I am happy that both of my modules share the same css, I just need two copies.
