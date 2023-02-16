### Simple Bulk-Rename-in-Node.js

Renamer is a command-line utility to help rename files and folders. It is flexible and extensible via plugins.

## Rename using JavaScript:
```
const fs = require('fs');
const replaceWith = "john"
const replaceThis ="manju"
const preview = true;

try {
  fs.readdir("data",(err,data)=>{

     console.log(data)
     for(let index =0;index<data.length;index++){
        const item = data[index];
        let newFile = "data/" + item.replaceAll(replaceThis,replaceWith)
        if(preview == false){
          fs.rename("data/"+item,newFile,()=>{
              console.log("renamed successfully")
          })

        }
        else{
          if("data/"+item !== newFile){
            console.log("data/"+item +" "+ "will rename to" +" "+newFile)
          }
        }
     }

    
})

} catch (err) {
  console.error(err);
}
```
### Usage:
 1.Use Only in Small Industrial Project
 2.Less Time Consuming
 
### Node FS Rename File
In this tutorial we will learn how to rename a file synchronously and asynchronously in Node.js using fs module.

Node FS Rename File – To rename file with Node FS, use fs.rename(new_file_name, old_file_name, callback_function) for asynchronous file rename operation and use fs.renameSync(new_file_name, old_file_name) for synchronous file rename operation. In this Node.js Tutorial, we shall learn syntax and examples for fs.rename() and fs.renameSync() functions of Node FS module.

### Syntax – fs.rename()
The syntax of rename() function is

fs.rename(new_file_path, old_file_path, callback_function)


