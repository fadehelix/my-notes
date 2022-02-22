## Memory management
#js/performance
https://felixgerschau.com/javascript-memory-management/





## Promise
#js/async
`Promise.all()` "wywala sie" jak tylko jeden promise sie zrejectuje. Zwraca tablice wartosci przekazanych w `resolve` albo wartosc tego feralnego `reject`.
`Promise.allSettled()`  jest zawsze resolved. Zwraca tablice obiektow ze statusem i wartoscia  w `resolve/reject`

```javascript
const resolvedOne = new Promise((resolve, reject) => {
  setTimeout(() => {resolve('resolvedONE!')}, 1000)
} )
const resolvedTwo = new Promise((resolve, reject) => {
  setTimeout(() => {resolve('resolvedTWO!')}, 3000)
})
const rejectedOne = new Promise((resolve, reject) => {
  setTimeout(() => {reject('rejectedONE :P')}, 60)
//   throw 'new Error('WTF!?')'
})

Promise.all([ resolvedOne, resolvedTwo, rejectedOne])
.then(
  value => console.log('Promise.all: ', value),
  value => console.log(value)
)
// Output: 'rejectedOONE :P'

Promise.allSettled([rejectedOne, resolvedOne, resolvedTwo])
.then(
value => console.log('Promise.allSettled: ', value)
)
/** 
Output: [
	{reason: 'rejectedONE :P', status: 'rejected'}
	{status: 'resolved', value: 'resolvedONE!'}
	{status: 'resolved', value: 'resolvedTWO!'}
]
*/
```


## React: Write performant code
### useMemo & useCallback
https://dev.to/nrf/reactmemo-is-your-friend-e6p

### memo()
