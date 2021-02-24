---
title: Progressive Web Apps vs Something Else
date: "2019-11-25T22:12:03.284Z"
---

A big part of my work right now is weighing the pros and cons of building a progressive web app vs something like React | Native. Time to market versus cost analyis. Time to market seems to win.

### For React

    1. Fewer cross-platform issues with React
       i. Responsiveness issues in Bootstrap.
       ii. React-Native looks much more 'native' in appearance as it uses OSX native features.
    2. React-Natives modular components allow you to reuse various parts of code across projects easily.
      i. Reusable modular components seem easier to build and keep consistent in React than in Bootstrap.
      ii. If I, for example, want to reuse the current menu on another restaraunt website it would be difficult to do so. To transfer one element from my current site to another would most likely cause the code to break. Each component is free-standing in React.
      iii. Component style programming accelerates efficiency, clarity, organization, etc. while creating less bugs overall.
    3. Bootstrap is designed for simple UI -- If I needed more custom UI features or when I will want to add some in the future I would likely want to re-write the site in React-Native.
    4. I can take advantage of many useful tools in React/React-Native such as automated unit testing (structural, interaction, css/style, etc.)
    5. Bootstraps grid system break points aren't ideal
       i. there were many times I did not want to style my element in a grid.
    6. Lots of code duplication, one for desktop another for mobile.
    7. Bootstrap is not meant for a production site that is looking to continuously deploy and improve upon its features.
    8.  React Storybook is nice for documentation.
    9.  If you are comfortable using Bootstrap you can import a library in React called [Reactstrap](https://reactstrap.github.io/) which integrates Bootstrap 4 into your React project.

All this being said I do not regret building the restaraunt sites first iteration with Bootstrap as it is very quick and easy to implement. Now that it is deployed I will, however, consider re-building the site using React sometime soon.
