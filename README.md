# VS Code Onigmo

Onigmo bindings for VS Code. This library is used in VS Code and is not intended to grow to have general Onigmo WASM bindings.

## Installing

```sh
npm install vscode-onigmo
```

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
