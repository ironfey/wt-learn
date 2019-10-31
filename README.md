# wt
 Learning the wt framework with cmake

Generating Visual Studio Solution
---------------------------------
`cmake -G "Visual Studio 15 2017 Win64" .` for Visual Studio 2017 Professional

Build with \
`cmake --build . --target ALL_BUILD --config Release` or\
`cmake --build . --target ALL_BUILD --config Debug`

Required manual fixes
---------------------
- Set `hello.wt` as StartUp project (right-click on project -> Set as StartUp project)
- For the Debug configurations: Under Project Properties->Linker->Input remove all non debug wt libs (e.g. wt.lib, debug version is wtd.lib)
- Ensure the .dll files are in your path

Running the application
-----------------------
To start from Visual Studio: \
Add to Project->Properties->Debugging->Command Arguments `--http-address=0.0.0.0 --http-port=8080 --docroot=.`

Access application from browser at `localhost:8080`