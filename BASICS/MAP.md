### Why is `Map` faster than `Object` for insert, delete, and lookup operations?
- **Key handling**
  - `Map`: Any data type can be used as a key.  
  - `Object`: Keys are always treated as strings.  
- **Performance impact**
  - In `Object`, type conversion occurs because of string-only keys.  
  - `Map` avoids this overhead, resulting in better performance.  
- **Usage guideline**
  - Use **Object** when working with a small amount of data that rarely changes.  
  - Use **Map** when handling large amounts of data with frequent operations.  
