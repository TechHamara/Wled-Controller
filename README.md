<div align="center" >
<h1><kbd>🏃‍♂️ WLED</kbd></h1>
An extension for MIT App Inventor 2.
</div>

## 📝 Specifications
* **
📦 **Package:** io.th.wled
💾 **Size:** 56.38 KB
⚙️ **Version:** 1.0
📱 **Minimum API Level:** 7
📅 **Updated On:** [date=2025-07-11 timezone="Asia/Calcutta"]
💻 **Built & documented using:** [FAST](https://community.appinventor.mit.edu/t/fast-an-efficient-way-to-build-extensions/129103?u=jewel) <small><mark>v2.8.4</mark></small>
* **

### 🤝 Multi-Components
1. [WLED](#kbd-wledkbd-3)
2. [WheelColorPicker](#kbd-wheelcolorpickerkbd-61)

# <kbd>🧩 WLED</kbd>
Developed by TechHamara using Fast.Extension to control WLED LED strips via HTTP<a href='https://t.me/techhamara91/' target='_blank'>Telegram</a> | <a href='https://github.com/TechHamara/' target='_blank'>GitHub</a><br><a href='https://buymeacoffee.com/techhamara/extras/' target='_blank'>BuyMeaCoffee</a> | <a href='https://m.youtube.com/c/TECHHAMARA?sub_confirmation=1' target='_blank'>YouTube</a><br><a href='https://github.com/TechHamara/Th_Free_Extensions' target='_blank'><small><u>Find More Extension</u></small></a><br><a href='https://github.com/TechHamara/Th_Extensions_List/blob/main/LICENSE.md#terms-and-conditions-for-the-extension' target='_blank'><small><u>Terms & Conditions</u></small></a>

## <kbd>Events:</kbd>
**WLED** has total 7 events.

### Response
Triggered when WLED returns a response.

| Parameter | Type
| - | - |
| response | text

### Error
Triggered when an error occurs.

| Parameter | Type
| - | - |
| error | text

### SyncResponse
Triggered when sync returns state.

| Parameter | Type
| - | - |
| response | text

### SyncError
Triggered when sync fails.

| Parameter | Type
| - | - |
| error | text

### InfoReceived
Triggered when WLED info JSON is received.

| Parameter | Type
| - | - |
| info | text

### Rebooted
Triggered when WLED device has rebooted.

### ConnectionStatus
Triggered when connection test to WLED device completes.

| Parameter | Type
| - | - |
| connected | boolean
| message | text

## <kbd>Methods:</kbd>
**WLED** has total 22 methods.

### Color
Set color. Provide R, G, B values (0-255).

| Parameter | Type
| - | - |
| r | number
| g | number
| b | number

### State
Fetch the current WLED JSON state.

### ColorAndEffect
Quickly set color + effect + brightness

| Parameter | Type
| - | - |
| r | number
| g | number
| b | number
| fx | number
| bri | number

### SavePreset
Save current state to a preset.

| Parameter | Type
| - | - |
| presetId | number
| name | text

### ClearSegments
Clear all segments.

### Segment
Set a segment with effect and color.

| Parameter | Type
| - | - |
| id | number
| start | number
| stop | number
| fx | number
| speed | number
| intensity | number
| rgb | list

### Transition
Send transition effect with fade and segment JSON.

| Parameter | Type
| - | - |
| fadeMillis | number
| jsonSegmentArray | text

### LoadSegmentFromString
Load segment config from JSON string.

| Parameter | Type
| - | - |
| jsonString | text

### EnableAutoSync
Enable auto state sync.

| Parameter | Type
| - | - |
| enable | boolean
| intervalMillis | number

### Toggle
Toggle WLED power state.

### GetInfo
Fetch WLED info JSON. Fires OnInfoReceived event.

### SegmentColor
Set color for a specific segment.

| Parameter | Type
| - | - |
| segmentId | number
| r | number
| g | number
| b | number

### Reboot
Reboot the WLED device. Fires OnRebooted event.

### DefaultColor
Set default color for WLED.

| Parameter | Type
| - | - |
| r | number
| g | number
| b | number

### Preferences
Fetch current WLED preferences (state JSON).

### Time
Get WLED device time.

### UsermodeGPIO
Get usermode GPIO configuration.

### MatrixSize
Set the matrix (panel) size for 2D effects. Requires ledmap.json to be present on the WLED device.

| Parameter | Type
| - | - |
| width | number
| height | number

### Segment2D
Set a 2D segment (rectangle) on the matrix/panel. Supports 2D options.

| Parameter | Type
| - | - |
| id | number
| start | number
| stop | number
| startY | number
| stopY | number
| fx | number
| pal | number
| rev | boolean
| rY | boolean
| tp | boolean
| rgb | list

### PanelLayout
Set the number of horizontal and vertical panels for a tiled matrix setup. Uploads ledmap.json.

| Parameter | Type
| - | - |
| horizontalPanels | number
| verticalPanels | number
| panelWidth | number
| panelHeight | number

### PanelWiring
Set panel wiring options: first LED position, orientation, serpentine, transpose. Uploads ledmap.json.

| Parameter | Type
| - | - |
| width | number
| height | number
| firstLedPos | text
| orientation | text
| serpentine | boolean
| transpose | boolean

### IndividualLEDs
Set the color of individual LEDs in a segment. Colors as hex strings (e.g. 'FF0000').

| Parameter | Type
| - | - |
| segmentId | number
| ledIndices | list
| colors | list

## <kbd>Setters:</kbd>
**WLED** has total 19 setter properties.

### IP
Set the WLED IP address.

* Input type: `text`

### Power
Turn WLED on or off.

* Input type: `boolean`

### Brightness
Set brightness 0-255.

* Input type: `number`

### Effect
Set effect ID.

* Input type: `number`

### Speed
Set effect speed (0-255).

* Input type: `number`

### Intensity
Set effect intensity (0-255).

* Input type: `number`

### Palette
Set palette ID.

* Input type: `number`

### ApplyPreset
Apply a preset.

* Input type: `number`

### DeletePreset
Delete a preset by ID.

* Input type: `number`

### LoadSegmentFromFile
Load segment config from file.

* Input type: `text`

### SingleColor
Set a single color using an integer (0xRRGGBB or 0xAARRGGBB). Alpha is ignored.

* Input type: `number`

### ARGBColor
Set ARGB color using integer (0xAARRGGBB). Alpha channel blends with existing colors.

* Input type: `number`

### AutoSync
Get or set auto sync state.

* Input type: `boolean`

### SyncInterval
Get or set sync interval in milliseconds.

* Input type: `number`

### White
Set white channel value (0-255).

* Input type: `number`

### DefaultBrightness
Set default brightness for WLED.

* Input type: `number`

### Time
Set WLED device time (ISO 8601 string).

* Input type: `text`

### TriggerMacro
Trigger a WLED macro by ID.

* Input type: `number`

### UploadLedMap
Upload a ledmap.json file to the WLED device for custom 2D mapping.

* Input type: `text`

## <kbd>Getters:</kbd>
**WLED** has total 5 getter properties.

### AutoSync
Get or set auto sync state.

* Return type: `boolean`

### SyncInterval
Get or set sync interval in milliseconds.

* Return type: `number`

### IsConnected
Get the current connection status.

* Return type: `boolean`

### ConnectionMessage
Get the last connection message.

* Return type: `text`

### CurrentIP
Get the current IP address.

* Return type: `text`

# <kbd>🧩 WheelColorPicker</kbd>
A color picker component developed by TechHamara using Fast technology, offering a user-friendly interface for selecting colors with various options such as wheel type, density, and sliders for lightness and alpha.<a href='https://t.me/techhamara91/' target='_blank'>Telegram</a> | <a href='https://github.com/TechHamara/' target='_blank'>GitHub</a><br><a href='https://buymeacoffee.com/techhamara/extras/' target='_blank'>BuyMeaCoffee</a> | <a href='https://m.youtube.com/c/TECHHAMARA?sub_confirmation=1' target='_blank'>YouTube</a><br><a href='https://github.com/TechHamara/Th_Free_Extensions' target='_blank'><small><u>Find More Extension</u></small></a><br><a href='https://github.com/TechHamara/Th_Extensions_List/blob/main/LICENSE.md#terms-and-conditions-for-the-extension' target='_blank'><small><u>Terms & Conditions</u></small></a>

## <kbd>Events:</kbd>
**WheelColorPicker** has total 4 events.

### ColorChanged
Event raised when the color is changed

| Parameter | Type
| - | - |
| newColor | number

### ColorSelected
Event raised when the color is selected

| Parameter | Type
| - | - |
| selectedColor | number

### WheelTypeChanged
Event raised when the wheel type is changed

| Parameter | Type
| - | - |
| newType | text

### ColorSelectedRGB
Event raised when the color is selected, returning separate R, G, B values

| Parameter | Type
| - | - |
| red | number
| green | number
| blue | number

## <kbd>Methods:</kbd>
**WheelColorPicker** has total 18 methods.

### Create
Initialize inside an arrangement.

| Parameter | Type
| - | - |
| arrangement | component

### ColorHex
Get the color of the picker as a hex string

* Return type: `text`

### ColorRGB
Set the color from RGB values

| Parameter | Type
| - | - |
| red | number
| green | number
| blue | number

### ColorRGBA
Set the color from RGBA values

| Parameter | Type
| - | - |
| red | number
| green | number
| blue | number
| alpha | number

### Red
Get the red component of the current color

* Return type: `number`

### Green
Get the green component of the current color

* Return type: `number`

### Blue
Get the blue component of the current color

* Return type: `number`

### AlphaValue
Get the alpha component of the current color

* Return type: `number`

### ColorHSV
Set the color from HSV values

| Parameter | Type
| - | - |
| hue | number
| saturation | number
| value | number

### Hue
Get the hue component of the current color

* Return type: `number`

### Saturation
Get the saturation component of the current color

* Return type: `number`

### Value
Get the value component of the current color

* Return type: `number`

### FlowerWheel
Set the wheel type to FLOWER

### CircleWheel
Set the wheel type to CIRCLE

### WheelTypeString
Get the current wheel type as string

* Return type: `text`

### SelectColor
Select the current color

### ShowDialog
Show the color picker dialog

### ShowDialogWithButtons
Show the color picker dialog with custom buttons

| Parameter | Type
| - | - |
| positiveButtonText | text
| negativeButtonText | text

## <kbd>Setters:</kbd>
**WheelColorPicker** has total 14 setter properties.

### Enabled
Get or set whether the color picker is enabled

* Input type: `boolean`

### Color
Get or set the current color

* Input type: `number`

### ShowAlpha
Get or set whether to show alpha channel

* Input type: `boolean`

### Lightness
Get or set the lightness value (0.0 to 1.0)

* Input type: `number`

### Alpha
Get or set the alpha value (0.0 to 1.0)

* Input type: `number`

### WheelType
Get or set the wheel type (0 for FLOWER, 1 for CIRCLE)

* Input type: `number`
* Helper type: `Type`
* Helper enums: `Flower`, `Circle`

### Density
Get or set the density of the color wheel (2-12)

* Input type: `number`

### DialogTitle
Get or set the dialog title

* Input type: `text`

### ShowLightnessSlider
Get or set whether to show lightness slider

* Input type: `boolean`

### ShowAlphaSlider
Get or set whether to show alpha slider

* Input type: `boolean`

### ShowBorder
Get or set whether to show border

* Input type: `boolean`

### ShowColorEdit
Get or set whether to show color edit

* Input type: `boolean`

### ShowColorPreview
Get or set whether to show color preview

* Input type: `boolean`

### PickerCount
Get or set the number of color pickers (1-5)

* Input type: `number`

## <kbd>Getters:</kbd>
**WheelColorPicker** has total 14 getter properties.

### Enabled
Get or set whether the color picker is enabled

* Return type: `boolean`

### Color
Get or set the current color

* Return type: `number`

### ShowAlpha
Get or set whether to show alpha channel

* Return type: `boolean`

### Lightness
Get or set the lightness value (0.0 to 1.0)

* Return type: `number`

### Alpha
Get or set the alpha value (0.0 to 1.0)

* Return type: `number`

### WheelType
Get or set the wheel type (0 for FLOWER, 1 for CIRCLE)

* Return type: `number`

### Density
Get or set the density of the color wheel (2-12)

* Return type: `number`

### DialogTitle
Get or set the dialog title

* Return type: `text`

### ShowLightnessSlider
Get or set whether to show lightness slider

* Return type: `boolean`

### ShowAlphaSlider
Get or set whether to show alpha slider

* Return type: `boolean`

### ShowBorder
Get or set whether to show border

* Return type: `boolean`

### ShowColorEdit
Get or set whether to show color edit

* Return type: `boolean`

### ShowColorPreview
Get or set whether to show color preview

* Return type: `boolean`

### PickerCount
Get or set the number of color pickers (1-5)

* Return type: `number`

