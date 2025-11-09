# TimePicki
Timepicki - FREE Timepicker JQuery plugin, simple and easy to understand, a clean way for your users to select times. Multiple initialization options and event callbacks for a higher degree of control and customization.

## Requirements
- JQuery 3.7.1 - [JQueryCDN](https://code.jquery.com/jquery-3.7.1.min.js) | [JsDelivr](https://cdn.jsdelivr.net/npm/jquery@3.7.1/dist/jquery.min.js)

## How to use
1. Include TimePicki Plugin js and css
```html
<link rel="stylesheet" type="text/css" href="path_to/timepicki.css">
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
    reset: false,
    input_writable: false
  };
```
| Option | Type | Default | Accepted values | Description |
| --- | --- | --- | --- | --- |
| increase_direction | String | 'up' | 'up', 'down' | Set increase hour or minute direction |
| custom_classes | String | '' | Any user declared string | Set custom classes to TimePicki |
| min_hour_value | Int | 1 | 0-23 integer | Set minimum selectable hour |
| max_hour_value | Int | 1 | 1-24 integer | Set maximum selectable hour |
| show_meridian | Bool | true | true, false | Toggle the meridian selector |
| step_size_hours | Int | 1 | >1 integer | Change the step size for hour increase/decrease | 
| step_size_minutes | Int | 1 | >1 integer | Change the step size for minute increase/decrease | 
| overflow_minutes | Bool | false | true, false | Update hours if minutes overflows over max or min |
| disable_keyboard_mobile | Bool | false | true, false | Prevent keyboard to show up on mobile (side effect: you can't type your hour on desktop keyboard) |
| reset | Bool | false | true, false | Resets to current time on TimePicki show |
| input_writable | Bool | false | true, false | Prevent input from being manually edited |

## Events
| Event | Description |
| --- | --- |
| show.modal.timepicki | This event fires immediately when TimePicki modal about to render |
| shown.modal.timepicki | This event fires immediately when TimePicki modal has been made visible to the user |
| change.time.timepicki | This event fires inmediately after user changes any value in TimePicki modal time controls |
| hide.modal.timepicki | This event is fired immediately when TimePicki modal close event has been called |
| hidden.modal.timepicki | This event is fired immediately when TimePicki modal has finished being hidden from the user |

<br/><br/>
## About maintainer and original developer
### Active Maintainer:
CollabWorkx is a next-gen work management platform that unifies collaboration, communication, and productivity. Built for flexibility and security, it empowers teams of all sizes to work smarter and achieve more—together. Learn more at: https://collabworkx.com/

### Original Developer:
I am senthil and I am  7+ years Frontend developer. Website: http://senthilraj.github.io/resume/

