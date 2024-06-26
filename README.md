# react-native-create-document-android

React Native Android module to use Android's Intent actions use the intent ACTION_CREATE_DOCUMENT.

You may need this functionality if you have to access device folders in an application that works on an Android version higher than 11

<https://developer.android.com/training/data-storage/shared/documents-files>

## Installation

```bash
npm i react-native-create-document-android
```

## Example

```javascript

import {createDocument} from 'react-native-create-document-android';

const FILE_CONTENT = 'some words in android file';

const callback = (uri: string) => {
  console.log('Saving file into: ' + uri);
  writeFile(uri, FILE_CONTENT); 
};

const testCreateDocument = () => {
  createDocument('test.txt', callback);
};

<View>
  <Text>Click here to save your file</Text>
  <Button title="save" onPress={testCreateDocument} />
</View>

```

## Example app

<https://github.com/jjorda/react-native-create-document-android-example>

## License

MIT
