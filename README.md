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
 Use Only in Small Industrial Project
 Less Time Consuming
 
 ### FrontEnd:
 Javascript (Node Js)


