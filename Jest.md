#jest

## Mocking document.querySelectorAll()

^435d9c

I want to test this function to be sure that it returns correct HTML:
```javascript
const getBoardContent = () => {

	const blocks = document.querySelectorAll('.Board .BlockContent');
	
	const html = Array.from(blocks)
		.map((block) => block.innerHTML)
		.join('');
	
	return html;
};

  

export default getBoardContent;
```

I need to provide custom HTML (mock the `blocks`  variable). Jest in CRA already uses the `jsdom` so I can just alter the `document` object.

```javascript

document.body.innerHTML = `<div class="Board">
	<div class="BlockContent">
		<p><strong>this is</strong> the content I want to test</p>
	</div>
</div>
```

## Mocking in general
[How to mock using Jest.spyOn](https://blog.echobind.com/how-to-mock-using-jest-spyon-d13d57a8434d)
[Mocking JS inner functions with Jest](https://chrisboakes.com/mocking-javascript-class-inner-functions-with-jest/)
