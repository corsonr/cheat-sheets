# console.log() Cheat Sheet


## Usefeul functions

| Command | Description |
| --- | --- |
| `console.log( 'message' )` | Prints "message" in the console |
| `console.assert( myVar, 'myVar is false' )` | Prints "myVar is false" if `myVar = false`, doesn't print anything if true |
| `console.table( obj )` | Displays nice formatted table |
| `console.group( 'Test' )` | Groups entries |
| `console.groupCollapsed( 'Test' )` | Groups entries collapsed by default |
| `console.dir( obj )` | Groups object attributes |
| `console.count()` | Increments a counter |
| `console.time()` | Starts a timer |
| `console.timeLog()` | End the timer and outputs time after last console.time() call |
| `console.trace( 'Start tracing' )` | Trace functions order |
| `console.log( '%c Sun is shining', 'color: #B54708; background-color: #FEDF89; font-weight: bold; padding: 5px; border-radius: 4px;' )` | Custom styling |
| `console.clear()` | Clears the console |
