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
[eternal] OK
0
1
2
Error: Something went wrong
   absolute/path/to/index.js:4:xx
   
[eternal] Process exited with none zero exit code
[eternal] Saving error log to 'error0.log'
[eternal] Restarting process
[eternal] Establishing io connection
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
}
```
