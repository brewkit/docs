# Architecture
Long-term maintenance is hard. Below you will find some standards and concepts we use to try to keep things simple, organized, and easy to maintain.
Keep in mind these assume a TypeScript + React stack.

<br>



## Component File Structure

Styles and types should be in their own files, separate from the meat of the component itself. So your typical file structure should look something like this:

```
|- components
    |- /Button
        |- index.tsx
        |- styles.ts
        |- tests.ts
        |- types.ts
```



### types.ts

Your types file should export the types necessary for your component and any additional type-related configuration necessary
for implementation of that specific component (i.e. module augmentation). Here is an example taken from the Brewkit Button component.

```ts
import * as React from 'react';
import { Theme, ThemeOptions } from '@material-ui/core/styles/createMuiTheme';
import { ButtonProps } from '@material-ui/core/Button';


/**
 * Declare any theme variables we want to make available.
 */
declare module '@material-ui/core/styles/createMuiTheme' {
    interface Theme {
        bkOverrides: {
            Button: {
                loading: React.CSSProperties,
            },
        },
    }
    // allow configuration using `createMuiTheme`
    interface ThemeOptions {
        bkOverrides: {
            Button?: {
                loading?: React.CSSProperties,
            },
        },
    }
}


export interface Props extends ButtonProps {

    /**
     * If `true`, the button will be disabled and show a spinner.
     * @default false
     */
    loading?: boolean,

}

```
