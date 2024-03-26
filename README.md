# vcredist

The Visual C++ redistributables

According to FLutter [documentation](https://docs.flutter.dev/platform-integration/windows/building#building-your-own-zip-file-for-windows) on how to prepare deployment for Flutter apps on Windows. It is mentioned that the following files are required:
- msvcp140.dll
- vcruntime140.dll
- vcruntime140_1.dll

There are [three options](https://docs.microsoft.com/en-us/cpp/windows/deployment-examples) on how we can include these files in the final app bundles, one of which is by using Application-Local folder.

On CI environment like GitHub action, we don't have the luxury much to install the C++ redistributables from [here](https://github.com/server-stack/vcredist) or [here](https://learn.microsoft.com/en-US/cpp/windows/latest-supported-vc-redist?view=msvc-170) and extract the dlls from there. A more straightforwad way is to just grab the required dlls from this repo, and bundle it togethers in the final `.exe` file.

The files were extracted from my PC on Path: `C:\Program Files (x86)\Microsoft Visual Studio\2022\BuildTools\VC\Redist\MSVC\14.36.32532\x64\Microsoft.VC143.CRT`.
