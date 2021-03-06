---
title: KeepAwake
---

A React component that prevents the screen sleeping when rendered. It also exposes static methods to control the behavior imperatively.

## Example: component

```javascript
import React from 'react';
import {
  Text,
  StyleSheet,
  View,
} from 'react-native';
import Expo, {
  Components
} from 'exponent';

class KeepAwakeExample extends React.Component {
  render() {
    return (
      <View>
        <Components.KeepAwake />
        <Text>This screen will never sleep!</Text>
      </View>
    );
  }
}

Exponent.registerRootComponent(KeepAwakeExample);
```

### Example: static methods

```javascript
import React from 'react';
import {
  Button,
  StyleSheet,
  View,
} from 'react-native';
import Expo, {
  Components,
} from 'exponent';

class KeepAwakeExample extends React.Component {

  _activate = () => {
    Components.KeepAwake.activate();
  }

  _deactivate = () => {
    Components.KeepAwake.deactivate();
  }

  render() {
    return (
      <View>
        <Button onPress={this._activate}>Activate</Button>
        <Button onPress={this._deactivate}>Deactivate</Button>
      </View>
    );
  }
}

Exponent.registerRootComponent(KeepAwakeExample);
```
