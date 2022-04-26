Rust
Thread safe
OpenXR / Vulkan inspired C API
Input runs on its own thread

## Interfaces
### Application Interface
#### Action Setup
```
struct ActionSetCreateInfo {
	name: String,
	priority: u32,
	needed_contexts: Vec<ActionContext>,?
}

fn createActionSet(create_info: &ActionSetCreateInfo) -> Result<ActionSet>;

struct ActionLayerCreateInfo {
	parent: ActionSet,
	name: String,
	needed_contexts: Vec<ActionContext>,?
	priority: u32,
}

fn createActionLayer(create_info: &SubActionSetCreateInfo) -> Result<ActionSet>;

struct ActionCreateInfo {
	action_set: ActionSet,
	name: String,
	action_type: ActionType,
}

fn createAction(create_info: &ActionCreateInfo) -> Result<Action>;

fn getChildAction(action: Action, identifier: Path) -> Result<Action>;
```
#### Text
<https://developer.android.com/training/keyboard-input>
<https://developer.apple.com/library/archive/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/KeyboardManagement/KeyboardManagement.html>
<https://www.w3schools.com/tags/tag_input.asp>
```
enum TextRequestType {
	Date,
	DateTime,
	Time,
	Email,
	Number {
		signed: bool,
		decimal: bool,
	},
	NumberPassword,
	PhoneNumber,
	Text {
		pattern: String,
		auto_correct: bool,
		cap_sentences: bool,
		cap_words: bool,
		cap_all: bool,
	},
}

struct TextRequestInfo {
	type: TextRequestType,
	end_action: EndAction,
	max_len: u32,
	cursor_idx: u32,
	auto_complete: bool,
	no_learning: bool,
	suggestions: Option<Vec<String>>,
	content: Arc<Mutex<String>>,
}
```
#### Binding
```
struct InputBindingConfig {
	source_settings: SourceSettings,
	component_conversion: Option<ComponentConversion>,
	activator: Option<Activator>,
	action_conversion: Option<ActionConversion>,	 
	action_settings: ActionSettings,
}
```
Action States
Action Contexts
Binding Layouts
Interaction Profiles
Glyphs
Players
Event Queue
Caching
Localization

### Driver Interface
Interaction Profiles
Input Components
Devices
Sync Stages
Event Pushers

### Loader Interface
GUI
