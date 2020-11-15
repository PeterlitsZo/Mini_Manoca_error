README
===============================================================================

Op
-------------------------------------------------------------------------------
1. `sudo npm install -g vue-cli`
   > I try to install the Vue's cli application.
2. `vue init simulatedgreg/electron-vue`
   > Use the template to init it, you can see more infomation by following this
   > link: https://simulatedgreg.gitbooks.io/electron-vue/content/.
3. Enter a lot of `enter`, so I get it by default setting.
4. `npm install`
   > Install other node library to make it can run.
5. `npm run dev`
   > It show that `HTML Webpack Plugin: ReferenceError: pocess is not defined`.
6. I follow https://github.com/SimulatedGREG/electron-vue/issues/871#issuecomment-490370237 to fix the bug.
   > Now I edit .electron-vue/webpack.web.config.js and .electron-vue/webpack.render.config.js,
   > by add a function `templateParameters` in `HtmlWebpackPlugin`.
   > Now it can run dev.
   > It show `Vue.js: 2.6.12`, `Electron: 2.0.18`, `Node: 8.9.3` and `Platform: linux`.
7. `npm run build`
   > Use 7m42s to download electron.zip... `>_<`, but run well.
8. Add the Manoco.
   > You can find the source at ./src/renderer/components/LandingPage.vue.
9. `npm install monaco-editor-webpack-plugin`.
10. `npm install monaco-editor`
11. `npm run dev`
    > looks great! There is a Monaco editor at here.
12. `npm run build`
    > Very slow... but why? And it raise a error like before...
    > This article says that I need to use monaco-editor-webpack-plugin,
    > I'd like to try:
    > https://zhuanlan.zhihu.com/p/47746336
13. Sad to see that:
    ```
    ERROR in renderer.js from Terser
    "o" is redeclared [renderer.js:1,260743]
    ```


