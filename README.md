# react-native-animateable-text

A `<Text/>` component that supports an Animated Value as text!

## Usage (Reanimated 2)

```tsx
import AnimateableText from 'react-native-animateable-text';

const Example: React.FC = () => {
  const text = useSharedValue('World');

  const animatedText = useDerivedValue(() => `Hello ${text.value}`);
  const animatedProps = useAnimatedProps(() => {
    return {
      text: animatedText.value,
    };
  });

  return (
    <AnimateableText
      text={animatedText}
      // same other props as Text component
    />;
};
```

<img src="https://user-images.githubusercontent.com/1629785/99287990-458d4600-283b-11eb-8d5e-0c1129189c89.gif">

## Installation

```sh
npm install react-native-animateable-text
```

## Usage

```js
import ReanimatedText from 'react-native-animateable-text';

// ...

const result = await ReanimatedText.multiply(3, 7);
```

## Contributing

See the [contributing guide](CONTRIBUTING.md) to learn how to contribute to the repository and the development workflow.

## License

MIT
