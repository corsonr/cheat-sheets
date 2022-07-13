# REACT Cheat Sheet

Sources:
- https://fr.reactjs.org/

## BASIC COMPONENT

```javascript
/**
 * External dependencies
 */
import PropTypes from 'prop-types';
import classnames from 'classnames';
import { __ } from '@wordpress/i18n';

/**
 * Internal dependencies
 */

const MyComponent = ( {
	className,
	propOne,
	propTwo,
} ) => {

	return (
		<div className={ classnames( 'my-class', className ) }>
			{__( 'this is the component', 'textdomain' )}
		</div>
	);
};

Countdown.propTypes = {
	className: PropTypes.string,
	propOne: PropTypes.string,
	propTwo: PropTypes.number,
};

export default MyComponent;
```

## INLINE FUNCTIONS
To pass an inline function to a component prop:

```javascript
myProp={ () => {
    // the function
} }
```
