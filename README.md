# UXPin-Storybook POC

The aim of this project is to integrate Storybook components developed with Svelte to UXPin in order to design applications.

## Storybook using Svelte components
Storybook is an open source tool for building UI components and pages in isolation. Among others, it is made for [Svelte](https://svelte.dev/).

Following the [**Introduction to Storybook for Svelte tutorial**] (https://storybook.js.org/docs/svelte/get-started/introduction), it has been developed a Storybook containing components to create a simple taskbox.

## UXPin
Once the Storybook is created, it can be used to design applications using [UXPin](https://www.uxpin.com/home). UXPin is a code-based design tool that merges design and engineering into one unified process.

### Storybook integration
The new feature being studied in this project is UXPin Merge. This includes Git integration and Storybook integration. This project is focused on investigating the possibilities that the latter offers. Storybook integration is used to bring fully interactive UI code-based components from Storybook and use them to design in UXPin. The main advantage is that it is possible to build prototypes that are consistent with all the design and development standards, by using the same components as the developers do. Moreover, designers are not required to know how to code since developers are in charge of it, and it is compatible with all Storybook frameworks (including Svelte). See the [documentation](https://www.uxpin.com/docs/merge/storybook-integration/).

To further study this feature, it has been designed a simple application using the public library Storybook Design System components.

### Drawbacks
The features considered in this study are in early stages in development. Next, it is exposed three different issues: Responsive Application, HTML Export, Production Code Export.

#### Responsive Application
By using the Storybook integration, it is not possible to create a responsive application. Although using responsive compoments, UXPin Merge can not use the component's media queries as the canvas is essentially fixed in size. So, even if it is done a window refresh to change the size of the canvas then it wouldn’t reflect in the components layout, resulting in a basic design.

This issue is solved in the Git integration case by creatin a React component named DeviceViewer, that functions as a wrapper, passing props and styles to a nested resizable IFrame component. When components are nested in the IFrame, they are no longer dealing with static canvas size, so all media queries, responsive properties, and styling will work perfectly.

#### HTML Export
This feature is in developemnt and has not full compatibility with Storybook. The UXPin support team response to the issue:
> As Storybook is still in early stages we don't have complete compatibility with the HTML export yet, as all the components are hosted and we are not saving all specs for such export yet. I would recommend using the Preview only for now.

#### Production Code Export
This feature is not yet developed. The UXPin support team response to the issue:
> Exporting your Prototypes as Production code is currently in progress, however, we don't have a specific date. We will certainly keep everybody up to date about this feature through our website and social media.