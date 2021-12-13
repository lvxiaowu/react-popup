<h1 align="center">Welcome to lxw-react-popup 👋</h1>
<p>
  <a href="#" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
  </a>
</p>

### 🏠 [Homepage](https://lvxiaowu.github.io/react-popup)

React Component based on `ReactDOM.createPortal` function for transportation element.

[React + TypeScript 从零开发 Popup 组件并发布到 npm](https://github.com/worldzhao/blog/issues/2)

## Install

```sh
yarn add lxw-react-popup

# or

npm i lxw-react-popup
```

## Usage

```jsx
import React, { useState } from 'react';
import { Popup } from 'lxw-react-popup';
import 'lxw-react-popup/dist/react-popup.min.css';

export default () => {
  const [visible, setVisible] = useState(false);
  return (
    <>
      <button onClick={() => setVisible(true)}>click me</button>
      <Popup maskClosable visible={visible} onClose={() => setVisible(false)}>
        <div className="your-content">hello world</div>
      </Popup>
    </>
  );
};
```

## API

| Property       | Description                                                                                    | Type                                           | Default  |
| -------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------- | -------- |
| visible        | Optional，control content visibility                                                           | boolean                                        | false    |
| position       | Optional，determines where the content will pop up                                             | 'center' / 'top' / 'bottom' / 'left' / 'right' | 'center' |
| mask           | Optional，decide whether to display the background layer                                       | boolean                                        | true     |
| maskClosable   | Optional，if the value is true, clicking on the background layer will trigger onClose function | boolean                                        | false    |
| onClose        | Optional，a function to set the visible to false                                               | function                                       | ()=>{}   |
| node           | Optional，the mounted node                                                                     | HTMLElement                                    | -        |
| destroyOnClose | Optional，whether content nodes are unloaded when closed                                       | boolean                                        | false    |
| wrapClassName  | Optional，className for the container node                                                     | string                                         | ''       |

## Contributions Welcome!

```sh
git clone git@github.com:lvxiaowu/react-popup.git
cd react-popup
yarn
yarn start
```

open another terminal tab

```sh
cd example
yarn
yarn start
```

## Run tests

```sh
yarn test
```

## Author

👤 **lvxiaowu**

## Show your support

Give a ⭐️ if this project helped you!

---

_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
