# kinetis_klxx_gcc using project generator

Note: This is using currently not released cmake support for pgen, to proceed, install a module from this branch please: https://github.com/project-generator/project_generator/tree/dev_v0.8 . Once pgen v0.8 is out, I'll remove this note.

This is a clone of kinetis_klxx_gcc repository. We don't use here any custom made makefile I wrote, but (project generator)[https://github.com/project-generator/project_generator].

## Use

The command below invokes pgen which generates files by default to generated_projects.

```
pgen export -f projects.yaml -p frdm-k64f-blinky -t cmake_gcc_arm
```

There should be a directory cmake_gcc_arm_frdm-k64f-blinky, where is the cmakelists. You can choose one of cmake options to generate makefile, sublime project and many more. I'll show how to proceed to generate Makefile and build a project.

Go into the generated_projects/cmake_gcc_arm_frdm-k64f-blinky , invoke
```
# Generates Makefile
cmake -G"Unix Makefiles"
# Builds the project
make
```

You should find built files in the build directory generated_projects/cmake_gcc_arm_frdm-k64f-blinky/build.
