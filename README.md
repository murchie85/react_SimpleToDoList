# SIMPLE TODO APPLICATION  
  
Learned how to do this from [fast youtube video](https://www.youtube.com/c/WebDevSimplified/videos)  
  
Stuff I learned.  
    

## USE STATE 

```js
const [values, functionToSetValues] = useState([])
```


## LOCAL STORAGE  


```js 

const LOCAL_STORAGE_KEY = 'todoApp.todo'

export default function App() {

  // INIT LIST ONCE
  useEffect( ()=>{
    // parse from storage key
    const storedList = JSON.parse(localStorage.getItem(LOCAL_STORAGE_KEY))
    if(storedList) setTodos(storedList)
  },[] )

  //  UPDATE ON CHANGE
  useEffect(()=>{
    localStorage.setItem(LOCAL_STORAGE_KEY, JSON.stringify(storedList))
  },[storedList])


```