# VSCode Onigmo

This [repo](https://github.com/RedCMD/vscode-Onigmo) is a fork of [vscode-oniguruma](https://github.com/microsoft/vscode-oniguruma).  
[TextMate 2.0](https://macromates.com/) uses [Onigmo](https://github.com/textmate/Onigmo/tree/Onigmo-5.13.5) for its regex engine.  
Onigmo is a modded version of oniguruma.  
[textmate/Onigmo](https://github.com/textmate/Onigmo) is a fork of [k-takata/Onigmo](https://github.com/k-takata/Onigmo) is a fork of [kkos/oniguruma](https://github.com/kkos/oniguruma).  

A few lines have been commented out in [onig.cc](/src/onig.cc).  
The `FindOption` `NotBeginPosition`, `NotBeginString` and `NotEndString` do not work.  
The faster `RegSet` API does not seem to exist in Onigmo.  
The updated [main.js](/release/main.js) and [onig.wasm](/release/onig.wasm) Onigmo files are located in the [release](/release/) folder.  
Onigmo keeps its `.c` files in the root directory, unlike oniguruma which keeps them in `./src`.  

This package is used in my VSCode TextMate extension https://marketplace.visualstudio.com/items?itemName=RedCMD.tmlanguage-syntax-highlighter  

Onigmo bindings for VSCode. This library can be used in VSCode and is not intended to grow to have general Onigmo WASM bindings.

## Installing

```sh
npm install vscode-onigmo
```
`vscode-onigmo` is let to be published to npm

## API doc

See [the main.d.ts file](./main.d.ts)

## Developing

* Clone the repository.
* Run `git submodule init`.
* Run `git submodule update`.
* Open the repository using the `Remote - Containers` extension, which will automatically create a docker container with the correct emscripten version and environment for building the WASM.
* Run `npm install`.
* Compile the Onigmo library with `npm run build-onig` (needed just once).
* Compile the `.wasm` with `npm run build-wasm` (needed every time the `onig.cc` file is changed).
* Compile the `.js` with `npm run build-tsc` or watch with `npm run watch-tsc` (needed every time the `.ts` files are changed).
* Package for releasing as UMD with `npm run package`

## Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Licenses
* [MIT](https://github.com/microsoft/vscode-oniguruma/blob/master/LICENSE.txt) microsoft/vscode-oniguruma
* [MIT](https://github.com/textmate/Onigmo?tab=License-1-ov-file) textmate/Onigmo
* [MIT](https://github.com/k-takata/Onigmo?tab=License-1-ov-file) k-takata/Onigmo
* [MIT](https://github.com/kkos/oniguruma?tab=License-1-ov-file) kkos/oniguruma

This project incorporates material from other projects. Please see [NOTICES.txt](https://github.com/microsoft/vscode-oniguruma/blob/master/NOTICES.txt)

## Thank you

Special thank you to [@lieene](https://github.com/lieene) for transfering the npm package name `vscode-oniguruma` to this project.
