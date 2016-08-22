# Snackbar Plugin

The Snackbar plugin allows you to display popup messages with an optional button.

## How to use

- Import the plugin to your project as explained [here](https://github.com/cobaltians/cobalt/wiki/Plugins-usage)
- Add the `cobalt.snackbar.js` to your web JS folder
- Add a html `<link>` to the `cobalt.snackbar.js` file after the cobalt link in the `<head>` tag

## Simple usage

Use the `cobalt.snackbar.show` shortcut:

    cobalt.snackbar.show('Native snackbar!');

## Complete usage

You can pass an object to `cobalt.snackbar.show` to specify more properties:

    cobalt.snackbar.show({
      text: 'Snackbar with button',
      duration: cobalt.snackbar.duration.SHORT,
      button: 'Dismiss',
      buttonColor: '#FF7700',
      callback: function () {
        cobalt.toast('Snackbar dismissed!');
      }
    });

Here are the available properties:

| Property | Type | Description |
|----------|------|-------------|
| `text` | String | The snackbar message |
| `duration` | Number | The snackbar duration time in milliseconds |
| `button` | String | The text of the button |
| `buttonColor` | String | The button hexadecimal color (see note on color below) |
| `callback` | Function | The button callback |

### Duration

If specified, the duration should be a value from the `cobalt.snackbar.duration` enum:

| Field | Description |
|-------|-------------|
| `SHORT` | A duration of 1.5 seconds |
| `LONG` | A duration of 2.75 seconds |
| `INFINITE` | Infinite duration |

__Note__: The `INFINITE` duration can only be used if a button is present.

### Button color

The button color must be provided as an hexadecimal code. Supported formats are `(#)RGB` or `(#)RRGGBB(AA)` (some valid examples: `#FF00BB`, `00FFEE`, `#666`, `1A3`, `#FF00BBAA`, `FF00BBAA`).

## Want more?

If you have any ideas or improvements to propose, please feel free to do so in the issue tracker!
