# accordion-init
Pure javascript library to use without any complex libraries

## version
v1.0.0

## usage
Include js, css, and img files. You can use minified js files for production usages.

## install the package
```
npm install accordion-init
```

###### Include files to use
```html
<link rel="stylesheet" href="dist/css/accordion.min.css">
<script src="dist/js/accordion.min.js"></script>  
```

###### Add HTML Template in .html file
```html
<div class="accordion-container">
	<div class="panel">
		<div class="heading">Panel Title</div>
		<div class="content">
			<p>
				Content
			</p>
		</div>
	</div>
	<div class="panel">
		<div class="heading">Panel Title</div>
		<div class="content">
			<p>Content</p>
		</div>
	</div>
	<div class="panel">
		<div class="heading">Panel Title</div>
		<div class="content">
			<p>Content</p>
		</div>
	</div>
</div>
```

###### Create accordion in javascript
```javascript
<script type="text/javascript">
	var accordion = new Accordion('.accordion-container');
</script>
```

###### Add HTML Template in .html file of your angularjs
```javascript
	$scope.accordion = new Accordion('.accordion-container');
```
If you're getting your content from server and takes a delay you should $timeout function.
```javascript
	$timeout(function() {
		$scope.accordion = new Accordion('.accordion-container');
	});
```

## API

###### Example
new Accordion(element, newSettings)

— element - string (obligatory), the html element you want to init as an accordion panel
— newSettings - object (optional), accordion settings you want to use. Check them in the following content

###### Settings

| Setting  | Type | Default | Description |
| ----- | ----- | ----- | ----- |
| hideAll | boolean | false | Hide all accordion panels at first time. Default: false |
| showAll | boolean | false | Hide all accordion panels at first time. Default: false |
| showFirst | boolean | false | Show a panel at first time. You should identify the panel number too: `panelId` |
| panelId | number | null | The panel number you want to show at first time. You should set true `showFirst` setting too. |

