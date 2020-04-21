# terse-b: Bunyan lib that is terse to use.

I noticed my log files were getting large. Also, I need loggin in each file. So I need something terse without to many LOC.

If node env is 'NODE_ENV=production' it will log only above INFO as JSON.
Else you get all w/ CLI.

eg: `env NODE_ENV=production node index.js`

Note: If you don't set above during DEV, ** you won't see the logs! **

Takes argument for class - to get name:

```
    import { TerseB } from "terse-b/terse-b"
    
    class C {

        log:any = new TerseB(this.constructor.name) // or hardcode the name

```

Result: 2 lines to set up logging, import and a decaration. In .js don't use `:any`,
 that is .ts syntax.



#### Performance mode for Express

- http://expressjs.com/en/advanced/best-practice-performance.html#set-node_env-to-production

