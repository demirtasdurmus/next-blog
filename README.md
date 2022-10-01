This is a starter template for [Learn Next.js](https://nextjs.org/learn).

  #npm run dev
    Starts the development server.

  #npm run build
    Builds the app for production.

  #npm start
    Runs the built app in production mode.

We suggest that you begin by typing:

  #cd nextjs-blog
  #npm run dev

## Using classnames library to toggle classes
classnames is a simple library that lets you toggle class names easily. You can install it using npm install classnames or yarn add classnames.

Please take a look at its documentation for more details, but here's the basic usage:

Suppose that you want to create an Alert component which accepts type, which can be 'success' or 'error'.
If it's 'success', you want the text color to be green. If it's 'error', you want the text color to be red.
You can first write a CSS module (e.g. alert.module.css) like this:

```
.success {
  color: green;
}
.error {
  color: red;
}
```

And use classnames like this:

import styles from './alert.module.css'
import cn from 'classnames'

```
export default function Alert({ children, type }) {
  return (
    <div
      className={cn({
        [styles.success]: type === 'success',
        [styles.error]: type === 'error'
      })}
    >
      {children}
    </div>
  )
}
```

