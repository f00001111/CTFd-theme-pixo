# CTFd-theme-pixo (Rewritten)

Rewritten version of the [CTFd-theme-pixo](https://github.com/hmrserver/CTFd-theme-pixo) theme based on [CTFd core](https://github.com/CTFd/CTFd/tree/master/CTFd/themes/core) theme by f00001111

Compatible with CTFd **Version 3.8.1**

Few Screenshots:
  
  ![Index Page](https://i.imgur.com/lL7zYrg.gif "Index Page")
  
  ![Challenge Page](https://i.imgur.com/o1XHK2t.png "Challenge Page")
  
  ![Challenge Popup](https://i.imgur.com/7YAQFs5.png "Challenge Popup")
  
  ![Score Board](https://i.imgur.com/COI4yAo.png "Score Board")
  
  ![Login Page](https://i.imgur.com/206O99m.png "Login Page")


### Installation Steps:
Open your Docker container's terminal then insert the following Command:
```
git clone -b 3.8.1 https://github.com/f00001111/CTFd-theme-pixo.git /opt/CTFd/CTFd/themes/pixo
```
Then Login as Admin and go to: ```Admin Panel > Config > Themes``` and switch the Theme to pixo and Click on Update.

That's it! Now you are good to goo..

## Tips
1. You can remove scanning line by remove [base.html(Line 42)](/templates/base.html#L42).
2. You can remove flicker by replace `animation:flicker .15s infinite` to `animation:none` in [main.xxxxxxxxx.css](/static/assets/main.1c8a8995.css).
3. You can also remove flicker by remove [main.scss(Line 134)](/assets/scss/main.scss#L134) and rebuild the theme using yarn.

## Custom License
1. User may edit the item, but can't replace My Theme Copyright & CTFd Copyright.
1. User need confirmation with us before removing copyright mark (footer).

## Creating Custom Theme (based on core-beta)

To create a custom theme based on the core-beta one, here are the steps to follow:

1. Clone core-beta theme locally to a seperate folder

   ```
   git clone https://github.com/CTFd/core-beta.git custom-theme
   ```

   To clarify the structure of the project, the `./assets` folder contains the uncompiled source files (the ones you can modify), while the `./static` directory contains the compiled ones.

2. Install [Yarn](https://classic.yarnpkg.com/en/) following the [official installation guides](https://classic.yarnpkg.com/en/docs/install).

   - **Yarn** is a dependency management tool used to install and manage project packages
   - **[Vite](https://vite.dev/guide/)** handles the frontend tooling in CTFd by building optimized assets that are served through Flask.

3. Run `yarn install` in the root of `custom-theme` folder to install the necessary Node packages including `vite`.

4. Run the appropriate yarn build mode:

   - Run `yarn dev` (this will run `vite build --watch`) while developing the theme.
   - Run `yarn build` (which will run `vite build`) for a one-time build.
     Vite allows you to preview changes instantly with hot reloading.

5. Now, you can start your modifications in the `assets` folder. Each time you save, Vite will automatically recompile everything (assuming you are using `yarn dev`), and you can directly see the result by importing your compiled theme into a CTFd instance.
   Note: You do not need the `node_modules` folder, you can simply zip the theme directory without it.

6. When you are ready you can use `yarn build` to build the production copy of your theme.

## Credits
- [Freepik](https://www.freepik.com "Freepik") For their awesome images (Arrow & Coin).
- [CTFd](https://github.com/CTFd "CTFd") For Creating such an Awesome Platform.

