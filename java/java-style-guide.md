# FRC 7034 Code Style Guide

## Table of Contents

1. [Introduction](#s1-introduction)

    1.1 [Guide Notes](#s1.1-guide-notes)

2. [Source File Basics](#s2-source-file-basics)

    2.1 [File Names](#s2.1-file-names)
    
3. [Source File Structure](#s3-source-file-structure)

4. [Formatting](#s4-formatting)

5. [Naming](#s5-naming)

6. [Programming Practices](#s6-programming-practices)

7. [Javadoc](#s7-javadoc)

8. [WPIlib Project Structure](#s8-wpilib-project-structure)

<h2 id="s1-introduction">1 Introduction</h2>

This document serves as the complete definition of FRC Team 7034 coding standards for WPIlib java robot projects.

Like other programming style guides, the issues covered span not only aesthetic issues of formatting, but other types of conventions or coding standards as well. However, this document focuses primarily on the hard-and-fast rules that we follow universally, and avoids giving advice that isn't clearly enforceable (whether by human or tool). 

Sections 1-7 are made up of relevant snippets from the [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html).

<h3 id="s1.1-guide-notes">1.1 Guide Notes</h3>

Example code in this document is non-normative. That is, while the examples are in Google Style, they may not illustrate the only stylish way to represent the code. Optional formatting choices made in examples should not be enforced as rules.

<h2 id="s2-source-file-basics">2 Source File Basics</h2>

<h3 id="s2.1-file-names">2.1 File Names</h3>

The source file name consists of the case-sensitive name of the top-level class it contains (of which there is exactly one), plus the .java extension.

<h2 id="s3-source-file-structure">3 Source File Structure</h2>

A source file consists of, in order:

1. License or copyright information, if present
2. Package statement
3. Import statements
4. Exactly one top-level class

<h3 id="s3.1-import-statements">3.1 Import Statements</h3>

<h4 id="s3.1.1-no-wildcard-imports">3.1.1 No Wildcard Imports</h4>

**Wildcard Imports**, static or otherwise, are **not** used.

<h4 id="s3.1.2-ordering-and-spacing">3.1.2 Ordering and Spacing</h4>

Imports are ordered as follows:

    1. All static imports in a single block.
    1. All non-static imports in a single block.

If there are both static and non-static imports, a single blank line separates the two blocks. There are no other blank lines between import statements.

<h3 id="s3.2-class-declaration">3.2 Class Declaration</h3>

<h4 id="s3.2.1-exactly-one-top-level-class-declaration">3.2.1 Exactly One Top Level Class Declaration"</h4>

Each top-level class resides in a source file of its own.

<h2 id="s4-formatting">4 Formatting</h2>

<h3 id="s4.1-braces">4.1 Braces</h3>

<h4 id="s4.1.1-use-of-optional-braces">4.1.1 Use of optional braces</h4>

Braces are used with if, else, for, do and while statements, even when the body is empty or contains only a single statement.

Other optional braces, such as those in a lambda expression, remain optional.

<h3 id="s4.2-column-limit">4.2 Column Limit: 100</h3>

Java code has a column limit of 100 characters. Any line that would exceed this limit must be line-wrapped.

Exceptions:
1. Lines where obeying the column limit is not possible (for example, a long URL in Javadoc)
2. `package` and `import` statements
3. Shell commands in comments

<h3 id="s4.3-line-wrapping">4.3 Line Wrapping</h3>

Terminology Note: When code that might otherwise legally occupy a single line is divided into multiple lines, this activity is called line-wrapping.

There is no comprehensive, deterministic formula showing exactly how to line-wrap in every situation. Very often there are several valid ways to line-wrap the same piece of code.

#### 4.3.1 Indent continuation lines at least +4 spaces

When line-wrapping, each line after the first (each continuation line) is indented at least +4 from the original line.

### 4.4 Modifiers

Class and member modifiers, when present, appear in the order recommended by the Java Language Specification: 

``java
public protected private abstract default static final transient volatile synchronized native strictfp
``

<h2 id="s5-naming">5 Naming</h2>

The words 'name' and 'identifier' will be used interchangeably in this section.

### 5.1 Rules common to all identifiers

Identifiers use only ASCII letters and digits.

### 5.2 Rules by Identifier Type

#### 5.2.1 Package names

Package names use only lowercase letters and digits (no underscores). Consecutive words are simply concatenated together. For example, `com.example.deepspace`, not `com.example.deepSpace` or `com.example.deep_space`.

#### 5.2.2 Class names

Class names are written in **UpperCamelCase**.

Class names are typically nouns or noun phrases. For example, `Character` or `ImmutableList`.

#### 5.2.3 Method names

Method names are written in lowerCamelCase.

Method names are typically verbs or verb phrases. For example, `sendMessage` or `stop`.

#### 5.2.4 Constant names

Constant names use UPPER\_SNAKE\_CASE: all uppercase letters, with each word separated from the next by a single underscore.

#### 5.2.5 Non-constant field names

Non-constant field names (static or otherwise) are written in lowerCamelCase.

These names are typically nouns or noun phrases. For example, `computedValues` or `index`.

#### 5.2.6 Parameter names

Parameter names are written in lowerCamelCase.

#### 5.2.7 Local variable names

Local variable names are written in lowerCamelCase.

### 5.3 Camel case: defined

See the canonical definition here. (https://google.github.io/styleguide/javaguide.html#s5.3-camel-case)

<h2 id="s6-programming-practices">6 Programming Practices</h2>

### 6.1 `@Override`: always used

A method is marked with the @Override annotation whenever it is legal. This includes a class method overriding a superclass method, a class method implementing an interface method, and an interface method respecifying a superinterface method.

### 6.2 Static members: qualified using class

When a reference to a static class member must be qualified, it is qualified with that class's name, not with a reference or expression of that class's type.
That is to say, only refer to static methods and fields using the class name itself, not by reference with another instance of the class.

<h2 id="s7-javadoc">7 Javadoc</h2>

At the _minimum_, Javadoc is present for every public class, and every public or protected member of such a class, with a few exceptions noted below.

    - Javadoc is not always present on a method that overrides a supertype method. 
    - Javadoc is optional for "simple, obvious" members like getFoo(), in cases where there really and truly is nothing else worthwhile to say but "Returns the foo".

Other classes and members have Javadoc as needed or desired. 

<h2 id="s8-wpilib-project-structure">8 WPIlib Project Structure</h2>

This is an example of a typical filetree for a command based WPIlib project.

```
src
 |-main
 | |-deploy
 | | |-pathplanner
 | | | |-navgrid.json
 | | | |-autos
 | | | |-paths
 | | |-swerve
 | |-java
 | | |-frc
 | | | |-robot
 | | | | |-commands
 | | | | | |-swervedrive
 | | | | | | |-auto
 | | | | | | | |-AutoBalanceCommand.java
 | | | | | | |-drivebase
 | | | | |-subsystems
 | | | | | |-swervedrive
 | | | | | | |-photonvision
 | | | | | | |-SwerveSubsystem.java
 | | | | |-Main.java
 | | | | |-Robot.java
 | | | | |-logging
 | | | | | |-SubsystemLogging.java
 | | | | |-Constants.java
 | | | | |-RobotContainer.java
```

### 8.1 Subsystem/Command file structure

Subsystems and commands consisting of multiple classes, either through utility classes or inheritence, must be within a package named after the subsystem.

Subsystems, but not their associated commands consisting of a single class may be without their own package.

```
-commands
 |-swervedrive
 | |-auto
 | | |-AutoBalanceCommand.java
 | |-drivebase
 | | |- ...
 | |-intake
 | | |- intakeCommand.java
-subsystems
 |-swervedrive
 | |-photonvision
 | | |- ...
 | |-SwerveSubsystem.java
 |-intakeSubsystem.java
 |-indexerSubsystem.java
```

### 8.2 Autogenerated files

The file paths of `Main.java`, `Robot.java`, `Constants.java`, and `RobotContainer.java` must not be changed from their defaults.

### 8.3 Utility classes

Utility classes may be placed in `src/main/java/frc/robot/` within an appropriately named package.

Do not create a `utils` package as it tends to become cluttered with garbage very quickly.

### 8.4 3rd party libraries

Additional configuration files for 3rd party libraries belong in `src/main/deploy/[Library Name]`

