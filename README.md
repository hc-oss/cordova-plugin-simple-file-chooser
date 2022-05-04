# Chooser

### Overview

This plugin is an forked version of cordova plugin chooser that provides multiple file selection functionality and removes base64 functionality as we can use ionic native file plugin to get file directly

### Installing

```sh
cordova plugin add cordova-plugin-simple-file-chooser
```

### Supported Platforms:

- Android
- iOS

### API

```js
/**
  * Displays native prompt for user to select one or more files.
  *
  * @param accept Optional MIME type filter (e.g. 'image/gif,video/*').
  *
  * @returns Promise containing selected files' information,
  * MIME type, display name, and original URI.
  *
  * If user cancels, promise will be resolved as undefined.
  * If error occurs, promise will be rejected.
  */
chooser.getFiles(accept?: string) : Promise<undefined|{
	mediaType: string;
	name: string;
	uri: string;
}>
```

### Example Usage

```js
(async () => {
  const file = await chooser.getFiles();
  console.log(file);
})();
```

### Note

If calling in typescript don't use types instead use direct javascript by `declare var chooser` on your ts file.
