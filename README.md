# TimePicki
TimePicki - FREE Timepicker jQuery plugin, simple and easy to understand, a clean way for your users to select times. Multiple initialization options and event callbacks for a higher degree of control and customization.
### Changelog
| Version | Date | Maintained? |
| --- | --- | --- |
| 3.0.2 | Nov 11th, 2025 | ✅ |
| 3.0.1 | Nov 11th, 2025 | ❌ |
| 3.0.0 | Nov 10th, 2025 | ❌ |

## Requirements
- jQuery 3.7.1 - [jQueryCDN](https://code.jquery.com/jquery-3.7.1.min.js) | [JsDelivr](https://cdn.jsdelivr.net/npm/jquery@3.7.1/dist/jquery.min.js)

## How to use
1. Include TimePicki Plugin js and css
```html
<link rel="stylesheet" type="text/css" href="path_to/timepicki.css">

<script type="text/javascript" src="path_to/jquery.min.js"></script>
<script type="text/javascript" src="path_to/timepicki.js"></script>
```
2. Identify or add your input for TimePicki to be attached to
```html
<input type="text" name="my_timepicker_name" class="my_timepicker_class"/>
```
3. Call TimePicki function with your input element selector of choice
```html
<script>
  $(function() {
    $(element).timepicki();
    // OR
    $(element).timepicki(options);
  });
</script>
```

## Options
```html
  let options = {
    increase_direction: 'up',
    custom_classes: '',
    min_hour_value: 1,
    max_hour_value: 12,
    show_meridian: true,
    step_size_hours: 1,
    step_size_minutes: 1,
    overflow_minutes: false,
    disable_keyboard_mobile: false,
    show_reset: false,
    theme: "dark",
    position: "bottom"
  };
```
| Option | Type | Default | Accepted values | Description |
| --- | --- | --- | --- | --- |
| increase_direction | String | 'up' | 'up', 'down' | Set increase hour or minute direction |
| custom_classes | String | '' | Any user declared string | Set custom classes to TimePicki |
| start_time | array | null | ["00", "00", "AM/PM"] | Set a start time |
| min_hour_value | Int | 1 | 0-23 integer | Set minimum selectable hour |
| max_hour_value | Int | 1 | 1-24 integer | Set maximum selectable hour |
| show_meridian | Bool | true | true, false | Toggle the meridian selector |
| step_size_hours | Int | 1 | >1 integer | Change the step size for hour increase/decrease | 
| step_size_minutes | Int | 1 | >1 integer | Change the step size for minute increase/decrease | 
| overflow_minutes | Bool | false | true, false | Update hours if minutes overflows over max or min |
| disable_keyboard | Bool | false | true, false | TimePicki inputs become readonly |
| show_reset | Bool | false | true, false | Adds a button that empties the input value and closes TimePicki |
| theme | String | "dark" | "dark", "light" | Changes the theme of TimePicki |
| position | String | "bottom" | "bottom", "top" | Changes the position of TimePicki |

## Events
| Event | Description | Return |
| --- | --- | --- |
| show.modal.timepicki | This event fires immediately when TimePicki modal about to render | .element (input) |
| shown.modal.timepicki | This event fires immediately when TimePicki modal has been made visible to the user | .element (input) |
| change.time.timepicki | This event fires inmediately after user changes any value in TimePicki modal time controls | .element (input) |
| hide.modal.timepicki | This event is fired immediately when TimePicki modal close event has been called | .element (input) |
| hidden.modal.timepicki | This event is fired immediately when TimePicki modal has finished being hidden from the user | .element (input) |
```html
<script>
  $(window).on('hidden.modal.timepicki', function (event) {
    // Do something like...
    console.log(`TimePicki closed with values set to ${event.element.getAttribute('data-timepicki-tim')}:${event.element.getAttribute('data-timepicki-mini')} ${event.element.getAttribute('data-timepicki-meri')}`);
    // OR if meridian is disabled do something like...
    console.log(`TimePicki closed with values set to ${event.element.getAttribute('data-timepicki-tim')}:${event.element.getAttribute('data-timepicki-mini')}`);
  });
</script>
```
## Attributes
| Attribute | Description |
| --- | --- |
| data-timepicki-tim | Hour |
| data-timepicki-mini | Minutes |
| data-timepicki-meri | AM/PM (Meridian - If enabled) |

<br/><br/>
## About maintainer and original developer
### Active Maintainer:
CollabWorkx is a next-gen work management platform that unifies collaboration, communication, and productivity. Built for flexibility and security, it empowers teams of all sizes to work smarter and achieve more—together. Learn more at: https://collabworkx.com/

### Original Developer:
I am senthil and I am  7+ years Frontend developer. Website: http://senthilraj.github.io/resume/

