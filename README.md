# eternal

```js
// index.js
let i = 0;
setInterval(() => {
 if (i > 3) {
   throw new Error('Something went wrong');
 } 
 console.log(i);
 i++;
}, 1000);
```
```terminal
$ npm i @olian04/eternal
$ npx eternal index.js
[eternal] Resolving path
[eternal] Starting process
[eternal] Establishing io connection
[eternal] Logs will be saved to 'index.js.log0.log'
[eternal] OK
0
1
2
Error: Something went wrong
   absolute/path/to/index.js:4:xx
   
[eternal] Process exited with none zero exit code
[eternal] Saving error log to 'index.js.error0.log'
[eternal] Restarting process
[eternal] Establishing io connection
[eternal] Logs will be saved to 'index.js.log1.log'
[eternal] OK
0
1
2
^C
[eternal] Received interrupt signal
[eternal] Terminating process
```

```js
// eternalrc.json
{
  "silent": false, // Disables all status logging done by eternal. 
  "debug": false, // Enables debug logs from eternal
  "no-log-saving": false, // Logs won't be saved to disk. 
  "no-error-saving": false, // Error messages won't be saved separately to disk.
  "log-path": ".", // Root path for which to store logs at. 
  "error-path": ".", // Root path for which to store errors at.
  "max-log-count": 0, // Maximum number of logs to be stored on disk before old ones are removed.
  "max-error-count": 0, // Maximum number of error logs to be stored on disk before old ones are removed.
  "restart-timeout": 0, // Number of milliseconds to wait before attempting to restart the process.
}
```
