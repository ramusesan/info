#Below command will fix the 

FATAL ERROR: CALL_AND_RETRY_LAST Allocation failed - JavaScript heap out of memory


```
set NODE_OPTIONS=--max_old_space_size=4096
```

Essentially, this error is saying that Node was unable to allocate enough memory for the script (in my case, webpack-config webpack.prod.js) that was executed when running npm run build.

```

"build": "set NODE_OPTIONS=--max_old_space_size=8192 && webpack --config webpack.prod.js",
"build-linux": "export NODE_OPTIONS='--max-old-space-size=8192' && webpack --config webpack.prod.js"

```
