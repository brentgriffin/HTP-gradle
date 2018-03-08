# HTP-gradle/projectInfo
Gradle code example for https://hightechprofessional.com

A gradle tasks for examining inputs and outputs of gradle tasks.

## Configurable variables:
    * maxInputListSize - Sets the threshold for whether or not to list the input file/directory names.  If total count of inputs are greater than this number, it will not list out each file/directory in detail.  This value defaults to 7.
    * maxOutputListSize = Sets the threshold for whether or not to list the output file/directory names.  If total count of outputs are greater than this number, it will not list out each file/directory in detail.  This value defaults to 7.
    * showFullPath - If false, only the file/directory name (last segment) is printed out.  If true, the full path name is printed out.  This value default to true.

## Other configuration:
  If your project dynamically updates the inputs and/or outputs of your tasks, you will need to make the projectInfo task dependent on your task so that it can run after your task and pick up the dynamic dependencies.  See first line in the task which is the commented out "dependsOn" - you can uncomment the line and change "taskName" to be the name of your task.

## Usage
  1.  Copy this task (or include it) into your Gradle build file (default name is build.gradle).
  2.  "gradle projectInfo"
  3.  Analyze output
