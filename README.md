# [Todo List](https://github.com/psaurav1290/todo-list)
This is my first react native follow-along project, a basic Todo List app.

### How to run
1. Clone the repository.
2. Move to the project directory.
3. Run - `npm install`
 5. Connect your device and enable USB debugging.
 6. Run- `expo start` 
 7. Press `a` for Android and `i` for IOS.
 8. For more options follow the console menu or open `http://localhost:19002/` on your browser to access Expo Developer Tools.

## Learning Outcomes
1. **Figma-**
The frontend was designed on Figma. The tool proves to be very helpful for designing and CSS properties could be easily copied and pasted on the destination stylesheet.
2.	**Expo-**
To install expo- `npm install --global expo-cli`
Expo tools are a great way to make development very convenient. The expo CLI provides commands to create a react native project- `expo inti todoList` and test them- `expo start` on emulator, on a physical devices available locally, over LAN or Tunnel, or right within a web browser. It uses Metro Bundler to bundle the live development version of app makes testing the app as simple as scanning a QR code. Also it is loaded with live editing feature with in-browser development tools.
3. **React Native Components-**
Got to learn about basic react native components-
- View- It is a container element analogous to div tag.
- Text- As the name suggests, it's used to display text.
- TextInput- Accepts text input
- TouchableOpacity- It is used to create a touchable area or simply a button.
- KeyboardAvoidingView- It is used to prevent a set of elements from hiding behind the input method (eg- when the keyboard shoots up). It is configured in the following way-
```
<KeyboardAvoidingView behavior={Platform.OS === "ios" ? "padding" : "height"}>
	<TextInput />
</KeyboardAvoidingView>
```
*All are imported from `react-native` module.*
```
import { KeyboardAvoidingView, Platform, StyleSheet, Text, TextInput, TouchableOpacity, View } from 'react-native';
```
4. **Applying styles-**
```
export default function App() {
	return (
		...
		<View style={styles.box}></View>
	)
}

const styles = StyleSheet.create({
	box: {
		height: 200,
		width: "90%",
	},
});
```
5. **Passing *props*-**
Props can be passed in a components as its attribute, eg- `<Component type={someType} />` and can be accessed in component as-
```
const Component = props => {
	return <Text>Type is {props.type}.</Text>
}
```
6. **Using state in functional component-**
Functional components can declare state variables, as in class-based views, using `useState()` hook.
```
const [state, setState] = useState(initialState);
```
`useState()` accepts an argument that sets the initial value of the state. It returns a stateful value, which can be used to access the state value, and a function to update its value.
