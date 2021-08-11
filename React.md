Axios API for retrieving data
 axios.get(location, { 
 params: { query: term},
 headers :{
 Authorization:"Client-ID: " }
 }).then(() => {
 response})
 
 responseis the data returned
 
 1st method .then
 
 2nd mark the func with async na d= const response = await axios()
 Get access key from EPOS NOW
 
For the seatch use an onChange Event  handler
value with refer to what the user has written

useState hook for defining multiple states of an object

useEffect hook use something like lifecycle methods
3 ways to configure it
component rendered for 1st time
component when it rerenders
when the data is changed  
useEffect arraw fn as the first args, Second arg when the code will be executed usually an array, 
[] initial, null initial rerender, [data] when the data is changed
Cant use async in useEffect create a fn inside fn for that or use the then (Arrow fn)

THrottle the number of API requests in a search
wait for 500ms and then make the request
setTimeout(Arrow fn, time)
clearTimout to cancel the ctime by passing the timeoutID from the previous timer
in the useEffect first arg func to make the effect is called and the cleanup fn can be returned

Dropdown
list of option passed as props
state will be the currently selected option
const [selected, setSelected] = useState(options[AnyValtoStartWith])
onClick{() => OnSelectedChange(option)}

useState to toggle open close the dropdown

useRef to get reference to a DOM element

DONT USE A TAG WITH REACT ROUTER

Google OAuth under Google +
OAuth ClientID
