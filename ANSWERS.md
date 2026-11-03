# Task 2 — Checkpoint answers

1. `onPress={handlePress}` passes the function to React Native so it can run when the user presses the component. `onPress={handlePress()}` calls the function immediately while the component renders.

2. `Button` is a simple, ready-made control with limited styling. `Pressable` is more flexible and is useful when custom layout, styling, pressed feedback, or interaction states are needed.

3. The `Pressable` style function receives an object containing interaction state such as `pressed` and returns a style object or an array of styles. For example: `style={({ pressed }) => [styles.button, pressed && styles.pressed]}`.

4. State variables should not be changed directly because React will not reliably schedule a render from a direct assignment. Use the setter returned by `useState`, such as `setIsFollowing(true)`.

5. `followers` is derived from `BASE_FOLLOWERS` and `isFollowing`, so storing it in a second state could create inconsistent values. A derived value is calculated from existing state and data during rendering.

6. A controlled `TextInput` gets its current value from React state and reports edits through a callback. The two key props are `value` and `onChangeText`.

7. `selectedSkills.push(skill)` mutates the existing state array. Create a new array instead, for example `setSelectedSkills((skills) => [...skills, skill])`, or use `filter` to remove an existing skill.
