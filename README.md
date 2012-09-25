- [Introduction](#introduction)
	- [Intention](#intention)
	- [Basic Principles](#basic-principles)
	- [Zen](#zen)
	- [Layout](#layout)
	- [Basic Warnnings](#basic-warnnings)
- [Categories](#categories)
	- [General Recomendations](#general-recomendations)
				- [Item:Struct Vs Classes](#itemstruct-vs-classes)
	- [Functions:](#functions)
				- [Item:Write Short functions](#itemwrite-short-functions)
	- [Comments](#comments)
				- [Item: All comments will be written in English.](#item-all-comments-will-be-written-in-english)
				- [Item: Use // for comments](#item-use--for-comments)
				- [Item: Use doxygen style comments](#item-use-doxygen-style-comments)
				- [Item: Avoid Unusefull comments.](#item-avoid-unusefull-comments)
				- [Item: Strategic Vs Tactical Comments.](#item-strategic-vs-tactical-comments)
				- [Item: What, Why and How](#item-what-why-and-how)
				- [Item: General Comments.](#item-general-comments)
				- [Item: Class Comments.](#item-class-comments)
				- [Item: Method declaration Comments.](#item-method-declaration-comments)
				- [Item: Method definition Comments.](#item-method-definition-comments)
	- [Classes](#classes)
		- [Constructors](#constructors)
				- [Item: How to handle a constructor that fails?](#item-how-to-handle-a-constructor-that-fails)
				- [Item: Default Constructor](#item-default-constructor)
				- [Item: Explicit Constructors](#item-explicit-constructors)
				- [Item: Copy Constructor and Assignment operator](#item-copy-constructor-and-assignment-operator)
				- [Item: Do the work in the constructor.](#item-do-the-work-in-the-constructor)
		- [Destructors](#destructors)
				- [Item: How to handle a destructor that fails...](#item-how-to-handle-a-destructor-that-fails)
				- [Item: Protect your class from being inherited or set your destructor as public and virtual.](#item-protect-your-class-from-being-inherited-or-set-your-destructor-as-public-and-virtual)
		- [Inheritance](#inheritance)
				- [Item: Prefer composition over inheritance.](#item-prefer-composition-over-inheritance)
				- [Item: Use public inheritance.](#item-use-public-inheritance)
				- [Item:Only use Multiple-Inheritance when dealing with Interfaces.](#itemonly-use-multiple-inheritance-when-dealing-with-interfaces)
		- [Interfaces](#interfaces)
		- [Operator Overloading](#operator-overloading)
				- [Item: Do not overload operators but in rare, special circunstances.](#item-do-not-overload-operators-but-in-rare-special-circunstances)
		- [Access control](#access-control)
				- [Item: Make your data members private](#item-make-your-data-members-private)
		- [Declaration order](#declaration-order)
				- [Item: Define the access control areas in the following order:](#item-define-the-access-control-areas-in-the-following-order)
				- [Item: Method definitions in the corresponding .cc file should be the same as the declaration order, as much as possible.](#item-method-definitions-in-the-corresponding-cc-file-should-be-the-same-as-the-declaration-order-as-much-as-possible)
	- [Scope](#scope)
				- [Item: Do not use unnamed namespaces](#item-do-not-use-unnamed-namespaces)
				- [Item: Choose the namespace name based on the project and possibly the path or the functional area](#item-choose-the-namespace-name-based-on-the-project-and-possibly-the-path-or-the-functional-area)
				- [Item: Do not use the "using" directive use namespace aliases.](#item-do-not-use-the-using-directive-use-namespace-aliases)
				- [Item: Nested classes.](#item-nested-classes)
				- [Item: Nonmember,Static Member and Globlal functions.](#item-nonmemberstatic-member-and-globlal-functions)
				- [Item: Local Variables.](#item-local-variables)
				- [Item: Static of global variables](#item-static-of-global-variables)
	- [Other C++ features](#other-c-features)
				- [Item:Default arguments.](#itemdefault-arguments)
				- [Item:Variable Length arrays](#itemvariable-length-arrays)
				- [Item: Friends](#item-friends)
				- [Item: Castings. Use C++ cast ( like static_cast) instead of C-style cast](#item-castings-use-c-cast--like-static_cast-instead-of-c-style-cast)
		- [Preincrement and PostIncrement](#preincrement-and-postincrement)
	- [Best practices](#best-practices)
	- [Files](#files)
				- [Item: All source files must include copyright information.](#item-all-source-files-must-include-copyright-information)
		- [Naming Files](#naming-files)
				- [Item: Always give a file a name that is unique in a context as large as possible.](#item-always-give-a-file-a-name-that-is-unique-in-a-context-as-large-as-possible)
				- [Item: No more than one public class for each header file.](#item-no-more-than-one-public-class-for-each-header-file)
				- [Item: Each implementation file should only have the methods for its class and those related.](#item-each-implementation-file-should-only-have-the-methods-for-its-class-and-those-related)
		- [Header Files](#header-files)
			- [Guard](#guard)
				- [Item: Guard All header files should have #define guards to prevent multiple inclusion](#item-guard-all-header-files-should-have-define-guards-to-prevent-multiple-inclusion)
			- [Dependencies](#dependencies)
				- [Item: Do not use an #include when a forward declaration would suffice](#item-do-not-use-an-include-when-a-forward-declaration-would-suffice)
				- [Item: Make header files self-sufficents](#item-make-header-files-self-sufficents)
				- [Item: All headers should be listed as descendant of the project's source directory without use of shortcuts](#item-all-headers-should-be-listed-as-descendant-of-the-projects-source-directory-without-use-of-shortcuts)
				- [Item: Avoid hidden dependencies including headers in the correct order.](#item-avoid-hidden-dependencies-including-headers-in-the-correct-order)
				- [Item: Avoid relative paths in #include directives!](#item-avoid-relative-paths-in-include-directives)
				- [Item: Use <> separators for third-party includes and "" separators for propietary files](#item-use--separators-for-third-party-includes-and--separators-for-propietary-files)
				- [Item:Use <modulename/headerfilename.h> to include headers from other modules.](#itemuse-modulenameheaderfilenameh-to-include-headers-from-other-modules)
				- [Item: Do NOT define entities with linkage in a header file](#item-do-not-define-entities-with-linkage-in-a-header-file)
			- [Inline](#inline)
				- [Item: Define methods as inline only when they are small and simple](#item-define-methods-as-inline-only-when-they-are-small-and-simple)
				- [Item: Do not define inline methods in the header file, usea a -inl.h file instead.](#item-do-not-define-inline-methods-in-the-header-file-usea-a--inlh-file-instead)
			- [Parameter order](#parameter-order)
				- [Item: Try to put input parameters first and output parameters last.](#item-try-to-put-input-parameters-first-and-output-parameters-last)
	- [Code Layout](#code-layout)
	- [Naming conventions](#naming-conventions)
		- [General rules:](#general-rules)
		- [Variables](#variables)
		- [Constants](#constants)
		- [Methods and Functions](#methods-and-functions)
		- [class / struct](#class--struct)
		- [Interfaces](#interfaces-1)
	- [Classes](#classes-1)
				- [Item: State explicit use of virtual keyword for virtual methods in hierarchy.](#item-state-explicit-use-of-virtual-keyword-for-virtual-methods-in-hierarchy)
				- [Item: Make data members private.](#item-make-data-members-private)
				- [Item: Do not create passive classes...](#item-do-not-create-passive-classes)
		- [Operator definitions.](#operator-definitions)
				- [Item: If needed, declare both comparison operators, and do it consistently.](#item-if-needed-declare-both-comparison-operators-and-do-it-consistently)
				- [Item: Protect assignment operators.](#item-protect-assignment-operators)
				- [Item: Do NOT overload operator&&, operator|| or operator, unless you have a VERY IMPORTANT reason](#item-do-not-overload-operator-operator-or-operator-unless-you-have-a-very-important-reason)
- [Best Practices](#best-practices-1)
	- [General](#general)
				- [Item: Avoid long methods. Avoid deep nesting](#item-avoid-long-methods-avoid-deep-nesting)
				- [Item: Do not use static objects in constructors](#item-do-not-use-static-objects-in-constructors)
				- [Item: Avoid type casting](#item-avoid-type-casting)
				- [Item: Use static class-scoped const instead of #define constants.](#item-use-static-class-scoped-const-instead-of-define-constants)
				- [Item: Use enum instead of a bunch of constants](#item-use-enum-instead-of-a-bunch-of-constants)
				- [Item: Use inline methods instead of function macros](#item-use-inline-methods-instead-of-function-macros)
				- [Item: Do not use goto](#item-do-not-use-goto)
				- [Item: Avoid magic numbers!](#item-avoid-magic-numbers)
				- [Item: Avoid using arrays as local variables or object fields](#item-avoid-using-arrays-as-local-variables-or-object-fields)
				- [Item: Use local variables on stack instead of heap.](#item-use-local-variables-on-stack-instead-of-heap)
				- [Item: Prefer initialization list on constructors](#item-prefer-initialization-list-on-constructors)
				- [Item: Compile cleanly at the highest warning level.](#item-compile-cleanly-at-the-highest-warning-level)
				- [Item: Do not use goto ( yes again )](#item-do-not-use-goto--yes-again-)
				- [Item: Encapsulate global variables, constants, enumerated types and typedefs inside a class](#item-encapsulate-global-variables-constants-enumerated-types-and-typedefs-inside-a-class)
	- [Design](#design)
				- [Item: Rely on types, not on representations. (DO NOT TRY TO X-RAY OBJECTS)](#item-rely-on-types-not-on-representations-do-not-try-to-x-ray-objects)
				- [Item: Prefer minimal classes to monolithic ones.](#item-prefer-minimal-classes-to-monolithic-ones)
				- [Item: One class one responsability](#item-one-class-one-responsability)
				- [Item: Do NOT give away your internals](#item-do-not-give-away-your-internals)
				- [Item: Avoid inherit from classes that were not designed to be base classes](#item-avoid-inherit-from-classes-that-were-not-designed-to-be-base-classes)
				- [Item: Avoid type switching, prefer polymorphism](#item-avoid-type-switching-prefer-polymorphism)
				- [Item: Prefer composition over inheritance](#item-prefer-composition-over-inheritance-1)
				- [Item: Inherit not to reuse, but to be reused.](#item-inherit-not-to-reuse-but-to-be-reused)
				- [Item: Provide abstract interfaces. Design for interfaces not for implementations.](#item-provide-abstract-interfaces-design-for-interfaces-not-for-implementations)
	- [Memory and Resource Management](#memory-and-resource-management)
				- [Item: Allocate storage only if you must](#item-allocate-storage-only-if-you-must)
				- [Item: Avoid using malloc and free. If you must do it be consistent](#item-avoid-using-malloc-and-free-if-you-must-do-it-be-consistent)
				- [Item: Do NOT use memcpy and memcmp to copy/compare anything more structured than a raw memory](#item-do-not-use-memcpy-and-memcmp-to-copycompare-anything-more-structured-than-a-raw-memory)
				- [Item: Always provide empty branches for deleting array objects](#item-always-provide-empty-branches-for-deleting-array-objects)
				- [Item: Postpone variable definition as long as posible](#item-postpone-variable-definition-as-long-as-posible)
				- [Item: Always assign a NULL value (0) to a deallocated pointer.](#item-always-assign-a-null-value-0-to-a-deallocated-pointer)
				- [Item: Avoid allocating and deallocating memory in different modules](#item-avoid-allocating-and-deallocating-memory-in-different-modules)
				- [Item: Use RAII idiom when possible ( Resource Acquisition IS Initialization) @todo:jlom Link](#item-use-raii-idiom-when-possible--resource-acquisition-is-initialization-todojlom-link)
	- [Methods](#methods)
		- [Return types and values](#return-types-and-values)
				- [Item: State return types for methods explicitly](#item-state-return-types-for-methods-explicitly)
				- [Item: A public method MUST NEVER return a NON-CONST reference or pointer to member data.](#item-a-public-method-must-never-return-a-non-const-reference-or-pointer-to-member-data)
				- [Item: NEVER return a pointer or reference to a local varibale.](#item-never-return-a-pointer-or-reference-to-a-local-varibale)
				- [Item: Minimize the number of temporary objects created as return values](#item-minimize-the-number-of-temporary-objects-created-as-return-values)
		- [Arguments](#arguments)
				- [Item: State argument names explicitly in declarations](#item-state-argument-names-explicitly-in-declarations)
				- [Item: Use references for arguments instead of pointers](#item-use-references-for-arguments-instead-of-pointers)
				- [Item: Limit default arguments](#item-limit-default-arguments)
				- [Item: Avoid methods with too many arguments](#item-avoid-methods-with-too-many-arguments)
				- [Item: Use array arguments instead of pointers](#item-use-array-arguments-instead-of-pointers)
				- [Item: Use argument passing modes to document the intention](#item-use-argument-passing-modes-to-document-the-intention)
				- [Item: Prefer references to pointers](#item-prefer-references-to-pointers)
				- [Item: Use const references for input parameters and non-const references for output parameters](#item-use-const-references-for-input-parameters-and-non-const-references-for-output-parameters)
				- [Item: If you have no other choice but to pass pointers as input parameters use type const * const construction.](#item-if-you-have-no-other-choice-but-to-pass-pointers-as-input-parameters-use-type-const--const-construction)
	- [Pointers and References](#pointers-and-references)
				- [Item: DO NOT compare a potinter to NULL or assign NULL to a pointer. Use 0 instead](#item-do-not-compare-a-potinter-to-null-or-assign-null-to-a-pointer-use-0-instead)
				- [Item: Use references instead of pointers whenever possible](#item-use-references-instead-of-pointers-whenever-possible)
				- [Item: Prefer references to pointer to pointer to pointer.](#item-prefer-references-to-pointer-to-pointer-to-pointer)
				- [Item: If you have to use NULL use it consistently.](#item-if-you-have-to-use-null-use-it-consistently)
	- [Const correcteness](#const-correcteness)
				- [Item: Use const for methods that should not affect the state of the object](#item-use-const-for-methods-that-should-not-affect-the-state-of-the-object)
	- [Type Conversions](#type-conversions)
				- [Item: When you have to make type cast USE C++ style cast.](#item-when-you-have-to-make-type-cast-use-c-style-cast)
				- [Item: Avoid reinterpret_cast unless you have a very good reason](#item-avoid-reinterpret_cast-unless-you-have-a-very-good-reason)
	- [Expressions](#expressions)
				- [Item: Use break instead of boolean flags in loops.](#item-use-break-instead-of-boolean-flags-in-loops)
				- [Item: Always use a default branch in switch statements](#item-always-use-a-default-branch-in-switch-statements)
				- [Item: Use typedef for function pointers](#item-use-typedef-for-function-pointers)
				- [Item: Parenthesis are free (as in free beer) .](#item-parenthesis-are-free-as-in-free-beer-)
				- [Item: Prefer prefix increment/decrement to the postfix variant.](#item-prefer-prefix-incrementdecrement-to-the-postfix-variant)
				- [Item: Always have non-lvalues ( constant ones ) on the left side of a comparison.](#item-always-have-non-lvalues--constant-ones--on-the-left-side-of-a-comparison)
	- [Error Handling](#error-handling)
				- [Item: Prefer compile-time and link-time errors to run-time errors](#item-prefer-compile-time-and-link-time-errors-to-run-time-errors)
				- [Item: Assert liberally to document internal assumptions and invariants](#item-assert-liberally-to-document-internal-assumptions-and-invariants)
				- [Item: Do not let any error to pass silently.](#item-do-not-let-any-error-to-pass-silently)
	- [Variables](#variables-1)
				- [Item: USE initialization semantic instead of assigment.](#item-use-initialization-semantic-instead-of-assigment)
				- [Item: Variables are declared with the smallest possible scope.](#item-variables-are-declared-with-the-smallest-possible-scope)
	- [Namespaces](#namespaces)
				- [Item: Use namespaces to avoid name collisions](#item-use-namespaces-to-avoid-name-collisions)
				- [Item: Use namespaces consistently](#item-use-namespaces-consistently)
				- [Item: Do not use using namespace clauses.Prefer alias instead](#item-do-not-use-using-namespace-clausesprefer-alias-instead)
	- [Virtuality](#virtuality)
				- [Item: Prefer to make base class virtual functions private (or protected if you really must).](#item-prefer-to-make-base-class-virtual-functions-private-or-protected-if-you-really-must)
				- [Item: Publicity vs. Privacy?](#item-publicity-vs-privacy)
- [Formatting](#formatting)
	- [Proposed style](#proposed-style)
- [Exceptions](#exceptions)
				- [Item: Always explicit which exceptions will throw your methods](#item-always-explicit-which-exceptions-will-throw-your-methods)
				- [Item: Use "Resource Acquisition Is Initialization" idiom.](#item-use-resource-acquisition-is-initialization-idiom)
	- [Project Directory Structure](#project-directory-structure)
		- [Item number %item_numer%](#item-number-item_numer)
		- [%Headline%](#headline)
			- [What](#what)
			- [Why](#why)
			- [Example:](#example)
			
<a id="Introduction"></a>
# Introduction
## Intention
The main goal of this document is to define a common way to develop in C++ providing recommendations and advises.
The code has to work, of course, but that its not enough. Software products are complex and have to be mantained for lon periods of time by a  huge number of persons with very differents backgrounds, that is why the maintanability and readability of the code is so important.
Remember:

Programs  that  are  developed  according  to  these  rules  and  recommendations should be correct and **easy to maintain**.  In order to reach these goals, the programs should:  

- Have a consistent style.  
	This way the code made by any team mate will seems less odd to you. We do not pretend everybody to write code exactly the same way, but some consistency will improve readability a lot.

- Be easy to read and understand.
	The code is written once but readed much more times and by very differents types of persons, so it should be as readable as possible.  
	Today we have a lot of development tools ( IDEs, code editors , ... ) which make the task of write code much more easier, so there is no reason to be lazy.

	Code should be written with this in mind, and also [well commented](#Comments), becasuse something that is cristal clear for you while you are involved in a development could be an arcane mistery for many of your work mates, or even for you three months later.

- be portable to other architectures. 

- be free of common types of errors
- be maintainable by **different programmers**. 

## Basic Principles

<a id="BasicPrinciples::DevilOptimization"></a>

- **"Premature optimization is the root of all evil in programming."**--C.A.R. Hoare 

<a id="BasicPrinciples::Incidentally"></a>
- Programs should be written for people to read, and only incidentally for machines to execute. --  Abelson and Sussman

<a id="BasicPrinciples::Fool"></a>
- "Any fool can write code that a computer can understand. Good programmers write code that humans can understand". --Martin Fowler
- "The belief that complex systems require armies of designers and programmers is wrong. A system that is not understood in its entirety, or at least to a significant degree of detail by a single individual, should probably not be built."

<a id="BasicPrinciples::CodeAutoDoc"></a>
- "Good code is its own best documentation. As you’re about to add a comment, ask yourself, ‘How can I improve the code so that this comment isn’t needed?’ Improve the code and then document it to make it even clearer." --Steve McConnell
- "It's OK to figure out murder mysteries, but you shouldn't need to figure out code. You should be able to read it."--Steve McConnell
- The code written for you three months ago is as 

<a id="Zen"></a>
## Zen 
**Beautiful** is better than ugly.  
**Explicit** is better than implicit.  
**Simple** is better than complex.  
Complex is better than complicated.  
**Flat** is better than nested.  
**Sparse** is better than dense.  
**Readability counts**.  
Special cases aren't special enough to break the rules.  
Although practicality beats purity.  
Errors should never pass silently.  
Unless explicitly silenced.  
In the face of ambiguity, refuse the temptation to guess.  
There should be one-- and preferably only one --obvious way to do it.  
Although that way may not be obvious at first.  
Now is better than never.  
Although never is often better than *right* now.  
If the implementation is hard to explain, it's a bad idea.  
If the implementation is easy to explain, it may be a good idea.  
Namespaces are one honking great idea -- let's do more of those! 

## Layout

## Basic Warnnings
- “A computer lets you make more mistakes faster than any other invention in human history, with the possible exceptions of handguns and tequila.” – Mitch Ratcliffe
- "Programming can be fun, so can cryptography; however they should not be combined." --Kreitzberg and Shneiderman


# Categories

## General Recomendations
##### Item:Struct Vs Classes
## Functions:
##### Item:Write **Short** functions

- Keep functions focused and small
- Prefer functions that do **ONE AND ONLY ONE** thing
- Even if your long function works perfectly now it is easy that someone modifying it in the near future will break it.



<a id="Comments"></a>
## Comments
Comments are one of the most important things to understand the code.  
Once a piece of software has been written to be easely readed and maintained the only thing to do is to explain those things that the code syntax do not allow to specify, here is where your friends "the comments" will help you.
But for the comments to be a useful tool instead of a burden they have to be seen as a part of the code, that have to be updated and also maintened. For that reason is essensial to write comments with important pieces of information, because nobody want to mantain something useless ( in the best of the cases) or even harmfull.

##### Item: All comments will be written in English.
We are working at an international environment so English is a must. @todo:jlom quizas esto no sea necesario.

##### Item: Use `//` for comments 
@todo: jlom Justificar esto.

##### Item: Use *doxygen* style comments

[Doxygen](http://www.doxygen.org) is a well known syntax for multiple programming languages and allow us to extract usefull technical documentation from the code itself, making your life easier. 

##### Item: Avoid Unusefull comments.

Consider the following simple statement:
    
    a = b;     // assign b to a   

The comment cannot communicate the meaning of the statement more clearly than the code itself, and so is **useless**.
Actually, it's **worse than useless**. It's deadly.
First, the comment distracts the reader from the code, increasing the volume of text the reader has to wade through in order to extract its meaning.
Second, there is  more source text to maintain, since **comments must be maintained** as the program text they describe is modified.
Third, this necessary maintenance is often not performed.

    c = b; // assign b to a 

A careful maintainer cannot simply assume the comment is an error and is obliged to trace through the program to  determine whether the comment is erroneous, officious (c is a reference to a), or subtle (assigning to c will later  cause the same assignment to be propagated to a somehow).

The line should originally have been written without a comment:

    a = b;

The code is maximally clear as it stands, with no comment to be incorrectly maintained.This is similar in spirit to the well-worn observation that the most efficient code is code that doesn't exist. The same applies to comments:  the best comment is one that didn't have to be written, because the code it would otherwise have described is self-documenting.

The common examples of unnecessary comments frequently occur in class definitions, either as the result of an  ill-conceived coding standard or as the work of a C++ novice:

    class C
    {
    // Public Interface
    public:
        C(void); // default constructor
        ~C(void); // destructor      
        // . . .
    };

You get the feeling you're reading someone's crib notes.
If a maintainer has to be reminded of the meaning of the `public:` label, you don't want that person maintaining your code.
None of these comments does anything for an C++ programmer except clutter the code and provide more source text to be improperly maintained.

    class C
    {
    // Public Interface
    protected:
        C( int ); // default constructor
    }; 

A **particularly odious** practice is that of inserting change logs as comments at the head or tail of source code files:

    /* 6/17/02 SCD fixed the gaforniflat bug */  


##### Item: Strategic Vs Tactical Comments.
Put comments before the code they are describing, do not use comments at the end of the line unless strictly needed. Comments are often said to be either strategic or tactical.A strategic comment describes what a function or section of code is intended to do, and is placed before this code. A tactical comment describes what a single line of code is intended to do, and is placed, if possible, at the end of this line. Unfortunately, too many tactical comments can make code unreadable.

##### Item: What, Why and How
These are the three questions a comment can answer.



##### Item: General Comments.
Every file containing source code must be docummented with and introductory comment that provides general information about the file functionality
@todo: jlom Construir unas templates en doxy tanto para el header como para el source file, asi como para las clases y los metodos.

##### Item: Class Comments.
Try to write a comment for each class/struct you write in the class header.
Remember that the header file is intended for the user of that class to be readed, so the main question you have to answer there is **WHAT** does this class?

##### Item: Method declaration Comments.
Again this is the *interface* of the method, so try to explain **WHAT** the method does.

- Specify any assumption about the input parameters: which are mandatory, which have default values and what are those values, ... etc
- Specify what are the output parameters, to let the user know what to spect from your method.

To specify your intentions ( what this piece of code is supossed to do ) will be a great tool in the future.


##### Item: Method definition Comments.
Here the comments are for those who will have to maintain your code.( Remember you will maintain your own code, so do not be lazy)
You haver already explaing *what* you are doing ( or at least what you want to do )
If the code is good enough you will not need to explain **HOW** are you doing it, but in very exceptional circumstances.
So, the main question you have to answer here is **WHY** : Most of the time this should be clear without any comment, but there will be situations where a comment will be necessary:

Example: You have to resolve some operation and, due to time restrictions or any other thing, you have to choose between two "not-so-good" solutions. Here is where a good comment explaing the two paths and why one of them have been choosen above the other can help a lot in the future.

Example: This is a very bad comment. Aside from the [*magic number*](http://stackoverflow.com/questions/47882/what-is-a-magic-number-and-why-is-it-bad), the most weird thing in this code is **why** the `index` variable is initialized to 34???! Maybe this is crystal clear for you while developing the method but, do you think it will be so clear for another person (or even yourshelf) in three months?

    uint32_t mymethod(void)
    {
        uint32_t index(34); //Initialize index < == >  BAD!!!!
        for (;index < MAX; ++index)
        {
            //do whatever
        }

        return index;
    }


This is a little [better](#BasicPrinciples::CodeAutoDoc):

    //This is the first byte we have to process because bytes from 0 to 33 belong to the header.
    /// @see http://internal/SASN/doc/packet for more info.
    const uint32_t PACKET_DATA_INI = 34; 

    ...

    uint32_t mymethod(void)
    {
        uint32_t index(PACKET_DATA_INI); 
        for (;index < PACKET_DATA_FIN; ++index)
        {
            //do whatever
        }

        return index;
    }



## Classes
### Constructors
##### Item: How to handle a constructor that fails?
Throw an exception.[See this](http://www.gotw.ca/gotw/066.htm)
##### Item: Default Constructor
**Always** define a default constructor if your class define member variables and has no other constructors
Initializing structures by default, to hold "impossible" values, makes debugging much easier.
##### Item: Explicit Constructors
Use `explicit` keyword for constructors with just one argument if you want to avoid [implicit conversion](poner un enlace).
Constructors with one argument are used automatically for conversion leading to unexpected behaviour.  

Example: 

    class Foo 
    { 
    public: 
        Foo( const int& x); 
    }; 
     
    int Function (const Foo& f); 
     
    int main(void 
    { 
        int x (4); 
        return Function(x); // Implicit ( and maybe undesired ) conversion. 
    };

##### Item: Copy Constructor and Assignment operator
Provide **both** of them when necessary, otherwise make them private with no implementation.
If you do not do this the compiler will create them for you and this could lead to **hard to find errors** regarding shallow copy and variable initialization.  
This is particulary important when your object has any pointer variable.


Example:

     class Foo
     {
     public:
         Foo(Data const * const ai_data) 
             : m_data(ai_data)
         {
             // nothing to do here
         }
         void Run(void)
         {
             m_data->ShowInfo();
             delete m_data;           //BAD delete
         }
     private:
         Foo(const Foo& ai_foo);             //private with no 
         Foo& operator=(const Foo& ai_foo);  // implementation

         Data* m_data;
     };

     void main(void)
     {
         Data* myData(new Data());
         Foo f1(myData);
         Foo f2(f1);             //ERROR copy construction not implemented
     }


If your class has a pointer member you **HAVE TO** define a copy constructor and an assignment operator

Example

     class Foo
     {
     public:
         Foo(Data const * const ai_data) 
             : m_data(ai_data)
         {
             // nothing to do here
         }
         void Run(void)
         {
             m_data->ShowInfo();
             delete m_data;           //BAD delete
         }
     private:
         Data* m_data;
     };
     
     void main(void)
     {
         Data* myData(new Data());
         Foo f1(myData);
         Foo f2(f1);                 //copy construction 
         f1->Run();
         f2->Run();                  //BOOM!!

         delete myData;
         myData = 0;
     };
If you **really** need to copy this class, you **have to implement** a copy-constructor...

     class Foo
     {
     public:
         Foo(Data const * const ai_data) 
             : m_data(ai_data)
         {
             // nothing to do here
         }
         Foo(const Foo& ai_foo) 
             : m_data(new Data(ai_foo.m_data))
         {
             // nothing to do here
         }
         void Run(void)
         {
             m_data->ShowInfo();
             delete m_data;           //BAD delete
             m_data = 0;              // Always !!
         }
     private:
         Data* m_data;
     };

##### Item: Do the work in the constructor.
Try to do all the object initialization in the constructor, do not relay on the object user calling an `init` method to initialize your object ... remember, users are bad ...


### Destructors
##### Item: How to handle a destructor that fails... 
Write a message to a log-file or call Aunt Tilda. But [**do not throw an exception!**](@todo:jlom poner un enlace)
##### Item: Protect your class from being inherited or set your destructor as `public` and `virtual`.
Inherit from a class with a non-virtual destructor will be a source of hard to find problems whenever a polymorphic destruction is done.  
So unless you want to use a class as a base class please protect it from unintended inheritance.

Prefer this way using the [Curiously Recurrent Template Pattern](http://en.wikipedia.org/wiki/Curiously_recurring_template_pattern)

     template< typename T > class Final
     {
     protected:
         Final(void) {}
         Final( Final const& ) {}
     };
     
     class X : private virtual Final<X>
     {
       // whatever I want to do
     public:
         int fun(void)
         {
             return 1;
         }
     };
     
     class Derived : public X
     {
         //empty class
     };
     
     int main(void) 
     {
         Derived obj;
         obj.fun();
     }
- This is another way:

     class _Final_
     {
     private:
         ~_Final_() {}
         friend class Final;
     };
     
     class Final : virtual public _Final_
     {
     public:
         int fun(void) { return 1; }
     };
     
     class Derived : public Final {};
     
     int main() 
     {
         Derived obj;
         obj.fun();
     }
*Note*: You can use [comeau compiler](http://www.comeaucomputing.com/tryitout/) to check this code snippets.

### Inheritance
##### Item: Prefer composition over inheritance.
Try to restrict use of inheritance to the **"is-a"** case: `Bar` subclasses `Foo` if it can reasonably be said that **`Bar` "is a kind of" `Foo`**.

##### Item: Use public inheritance.
Unless you have a very interesting reason, If you think you have to use `private` inheritance use *composition* instead

##### Item:Only use Multiple-Inheritance when dealing with Interfaces.
Multiple-Inheritance is a quite sharp knife so unless you know what are you doing pretty well ( and also explain it to others in the comments very well ) do not use it but for [Interfaces](#Interfaces).
If you are thinking to use it even after this advise please take a look at `virtual` inheritance.

<a id="Interfaces"></a>
### Interfaces
Remember the [Program to interfaces not implementations](http://stackoverflow.com/questions/2697783/what-does-program-to-interfaces-not-implementations-mean) principle.  
Interface Characteristics:

- It has only public pure virtual methods and static methods  
- It has not non-static data members  
- It has no constructor defined  
- If it is a subclass it may only derive from classes that satisfy these conditions ( Interfaces)  
- Its name should start with a capital i 'I' and usally define some behavoiur  
- Always declare a virtual (non-pure)  destructor to make sure that your interfaces can be destroyed correctly

### Operator Overloading
##### Item: Do not overload operators but in rare, special circunstances.
Although operator overloading can make code more intuitive it has some problems: 

- It can fool your intuition into thinking that expensive operations are cheap built-in operations. 

- It is much harder to find where the overloaded operators are called. It is easy to search for "Equals()" than to search for "==" 

- Some operators work on pointers too, making very easy to introduce hard to find bugs. *Example*: `Foo+4` is totally different to `&Foo + 4`

### Access control
##### Item: Make your data members private

### Declaration order
##### Item: Define the access control areas in the following order:

- `public`
- `protected`
- `private`

The `public`, `protected` and `private` sections of a class should be explicitly delcared in that order. This way the first thing someone will see is the public section of your class that is the interface a user needs to know to use your class. 

Try not to repeat any of them.  
Within each section, the declarations **generally** should be in the following order:

- Typedefs and Enums  
- Constants (static const data members) 
- Constructors 
- Destructor 
- Methods, including static methods 
- Data Members (except static const data members)

##### Item: Method definitions in the corresponding .cc file should be the same as the declaration order, as much as possible.

## Scope
##### Item: Do not use unnamed namespaces
##### Item: Choose the namespace name based on the project and possibly the path or the functional area
##### Item: Do not use the "using" directive use namespace aliases.
Namespaces subdivide the global scope and provide a hierarchical axis of naming, helpping to avoid name collisions,"using" directive make all the names from a namespace available in another namespace breaking the namespace division.
##### Item: Nested classes.
Use private nested classes when the nested class is used only by the enclosing classThis way you do not pollute the global namespace with a class that is only a tool for another class.
Do **not** use public nested classes unless they are part of an interface.
##### Item: Nonmember,Static Member and Globlal functions.
- Prefer *static Member Methods* over *nonmember functions*
- Prefer *nonmember functions* within a namespace to *global functions*.
- **Avoid** the use of *completely global functions* as much as possible.

Sometimes it is necessary to define a function not bound to a class instance.Such a function can be either a static member or a nonmember function. 
Nonmember functions should not depend on external variables, and should nearly always exist in a namespace.   

Rather than creating classes only to group static member functions which do not share static data, **use namespaces** instead.

##### Item: Local Variables.
Place local variables in the **narrowest** scope possible.
Always initialize variables in the declaration
Use constructor semantics instead of assigment semmantics.
Explain why have you choose that specific initialization value whe it is not evident.  

**Example**:
        ConnectionData trsDbConnectionData;
        trsDbConnectionData = trsDb.GetConnectionData(); //BAD!!
        //---------------------
        ConnectionData trsDbConnectionData = trsDb.GetConnectionData(); // better
        //---------------------
        ConnectionData trsDbConnectionData(trsDb.GetConnectionData()); // MUCH BETTER

##### Item: Static of global variables
The use of static or global variables of class type is **strongly discourage**: they cause hard-to-find bugs due to indeterminate order of construction and destruction.


Objects with static storage duration, including global variables, static variables, static class member variables, and function static variables, **must be Plain Old Data (POD)**:
- ints
- chars
- floats
- pointers
- arrays/structs of POD.


The order in which class constructors and initializers for static variables are called is only **partially specified** in C++ and **can even change from build to build**, which can cause bugs that are difficult to find. 
Therefore in addition to banning globals of class type, we do not allow static POD variables to be initialized with the result of a function, unless that function (such as getenv(), or getpid()) does not itself depend on any other globals.
Likewise, the order in which destructors are called is defined to be the reverse of the order in which the constructors were called. 
Since constructor order is indeterminate, so is destructor order. 
For example:
at program-end time a static variable might have been destroyed, but code still running tries to access it and fails. Or the destructor for a static 'string' variable might be run prior to the destructor for another variable that contains a reference to that string.  As a result we only allow static variables to contain POD data.

## Other C++ features
##### Item:Default arguments.
Avoid default arguments as much as you can.
Default paremeters can lead to situations where default values are used silently for some arguments.

##### Item:Variable Length arrays
Do not use them, they **are not part of Standard C++** and allocate a data-dependent amount of stack space that can trigger difficult to find memory errors

##### Item: Friends
Avod the use of the "friend" keyword but with a very good reason
##### Item: Castings. Use C++ cast ( like static_cast) instead of C-style cast
C++ cast allow you to differenciate when you are making a conversion ( `(int)3.5`) or a cast ( `(int) "hello"` )  
It is easier to search for C++-style cast than for C-style cast.  
**Note**:

- Use **`static_cast`**  as the equivalent of a C-Style cast that do a conversion or for upcast a pointer to a baseclass. 
- Use **`const_cast`** to remove a const qualifier ( WARNING: Use it with care!! ) 
- Use **`reinterpretet_cast`** ... never or almost never! This is a **totally unsafe** conversion 
- Do not use **`dynamic_cast`**.todo: jlom Justificar esto o relajarlo un poco

### Preincrement and PostIncrement
Whenever you do not need to know the value of the object *before* the increment **use the preincrement**.  
[Why?:](http://stackoverflow.com/questions/2020184/preincrement-faster-than-postincrement-in-c-true-if-yes-why-is-it)  
Postincrement method returns the current value of the object, then make the increment and return the value of the object again, while the preincrement just incremente the object and returns its value.
The difference it is just an operation, but this operation ( a copy constructor or an assigment operator call ) could be heavy. todo: jlom poner un enlace
## Best practices

## Files
##### Item: All source files must include copyright information.

### Naming Files
##### Item: Always give a file a name that is unique in a context as large as possible.
A header file for a class should have a file name of the form <class_name>.h.  
Use  uppercase  and  lowercase  letters  in  the  same  way  as  in  the source code.
Since  class  names  must  generally  be  unique  within  a  large  context,  it  is appropriate  to  utilize  this  characteristic  when  naming  its  header  file.
This convention makes it easy to locate a class definition using a file-based tool. 

##### Item: No more than one public class for each header file.
This make easy to locate a class interface .

##### Item: Each implementation file should only have the methods for its class and those related.
This make easy to understand a class implementation because all the methods regarding its funcionality are together.

### Header Files
#### Guard

##### Item: Guard All header files should have #define guards to prevent multiple inclusion
The format of the symbol name could be **"\_\_%PROJECT_PATH%\_%FILENAME%\_H\_\_"**. 
To guarantee uniqueness, they should be based on the full path in a project's source tree. 
For example, the file foo/src/bar/baz.h in project foo should have the following guard: 

	#ifndef __FOO_BAR_BAZ_H__ 
	#define __FOO_BAR_BAZ_H__
	... 
	#endif // __FOO_BAR_BAZ_H__

#### Dependencies

##### Item: Do not use an #include when a forward declaration would suffice
When you include a header file you introduce a dependency that will cause your code to be recompiled whenever the header file changes. If your header file includes other header files, any change to those files will cause any code that includes your header to be recompiled. Therefore, we prefer to minimize includes, particularly includes of header files in other header files.  You can significantly reduce the number of header files you need to include in your own header files by using forward declarations. 
For example, if your header file uses the File class in ways that do not require access to the declaration of the File class, your header file can just forward declare

	class File; 
    
instead of having to

	#include "file/base/file.h".  

How can we use a class Foo in a header file without access to its definition?  

- We can declare data members of type Foo* or Foo&(prefer).
- We can **declare** (but **not define**)@todo:jlom Incluir un link con la diferencia entre declarar y definir en C++ functions with arguments, and/or return values, of type Foo. (One exception is if an argument Foo or const Foo& has a non-explicit, one-argument constructor, in which case we need the full definition to support automatic type conversion.) 
- We can declare static data members of type Foo. 

On the other hand, you must include the header file for Foo if your class subclasses Foo or has a data member of type Foo.
Sometimes it makes sense to have pointer (or better, scoped_ptr) members instead of object members. However, this complicates code readability and imposes a performance penalty, so avoid doing this transformation if the only purpose is to minimize includes in header files.  Of course, .cc files typically do require the definitions of the classes they use, and usually have to include several header files. 

##### Item: Make header files self-sufficents
Every implementation file must include the relevant files that contain:
- declarations of types and functions used in the functions that are implemented in the file.
- declarations of variables and member functions used in the functions that are implemented in the file.  

##### Item: All headers should be listed as descendant of the project's source directory without use of shortcuts
**Example**: To include the header file `"RGsession.h"` from the module NSPrelay we should write : `#include "NSPrelay/RGSession.h"`

##### Item: Avoid hidden dependencies including headers in the correct order.
To avoid hidden dependencies includes should be done in the following order: 
- Your project header files. 
- Other libraries header files 
- C system files 
- C++ system files.

**Example**: In RGSession.cc the include list will be: 

	#include "RGSession.h" 
	#include "NSfw/basicTypes.h" 
	#include "NSPrelay/ControllableSession.h" 
	#include <sys/types.h> 
	#include <vector> 

This way if RGSession.h omits some necessary includes the compilation will break to those working on the RGSession.h/RGSession.cc files not for innocent people in other packages.

##### Item: Avoid relative paths in #include directives! 
@todo:jlom Justificarlo

##### Item: Use <> separators for third-party includes and "" separators for propietary files
@todo:jlom Justificarlo

##### Item:Use `<modulename/headerfilename.h>` to include headers from other modules. 
Compiler  include  paths  should  always point  to  the root directory of the project ( where all the modules are ) . Therefore, if a header file is located in another module,  it  must  be  included  with `#include <dir/filename.h>`

As a positive side effect, this avoids name clashes if different projects have a header file with the same name.

##### Item: Do **NOT** define entities with linkage in a header file
@todo:jlom Justificarlo

#### Inline
##### Item: Define methods as inline only when they are small and simple
Inlining a method can generate more efficient object code, but only if the method itself is small, simple ( without loops, switch ... ).

- Do not put large method definitions inline in the class definition.   Usually, only trivial or performance-critical, and very short, methods may be defined inline.
- Do not inline Constructors and Destructors. They are bigger than it seems  

*Note*: Remember that inline is just a hint to the compiler so even if you define a method as inline the compiler can choose not to inline it.

##### Item: Do not define inline methods in the header file, usea a `-inl.h` file instead.
Define all inline methods, except the simplest ones, in a separate header file called `<classname>-inl.h` and include it after the class declaration.  
This help to keep the header of your class *as readable as possible* and so it will be easier to know what your class is intended to do.

*File MyClass.h*

    #ifndef __MYPROJECT_MYNAMESPACE_MYCLASS_H__ 
    #define __MYPROJECT_MYNAMESPACE_MYCLASS_H__ 
    class MyClass 
    { 
        public:
        MyClass(void);
        virtual ~MyClass(void);
        uint32_t GetValue(void) const
        {
            return m_value;
        }
        void SetValue(const uint32_t& ai_value) 
        {
            m_value = ai_value;
        }
        bool DecrementValue(void);
        protected:
        private:
        uint32_t m_value;
    };
    #include "MyClass-inl.h"

*File MyClass-inl.h*

    #ifndef __MYPROJECT_MYNAMESPACE_MYCLASSINL_H__ 
    #define __MYPROJECT_MYNAMESPACE_MYCLASSINL_H__ 

    inline bool MyClass::DecrementValue(void)
    {
        if ( 0 < m_value )
        {
            --m_value;
        }
        return ( 0 != m_value);
    }
    #endif // __MYPROJECT_MYNAMESPACE_MYCLASSINL_H__ 

And then include the file at the end of the header file.
This way you do not polute the header file and the interface of a class is easier to read and understand.
Example:

*File:MyClass.h*

	class MyClass
	{
	public:
		inline AMethod(const int32_t& ai_id);

	protected:
		inline AnotherMethod(const String& ai_name);
	private:
		inline LastMethod(const uint64_t& ai_data);
	};
	#include "MyClass-inl.h"


*File:MyClass-inl.h*


	MyClass::AMethod(const int32_t& ai_id)
	{
		//do things here ...
	}

	MyClass::AnotherMethod(const String& ai_name)
	{
		//do things here
	}

*File:MyClass.cc*


	MyClass::LastMethod(const uint64_t& ai_data)
	{  
		//do things here 
	}

*Note*: Remember:

- `inline` keyword is only used in definition not in declaration. @todo:jlom Justificar.
- `inline` methods have to be present in the same compilation unit as the code who calls them thats why we have to define them in a header file, but `inline` `private` methods should only be called from inside the class, so they can be defined in the `.cc` file.

#### Parameter order
##### Item: Try to put input parameters first and output parameters last.


<a id="CodeLayout"></a>
## Code Layout

## Naming conventions
The main target is to make easier for other developers to read and understand the code you have written.

### General rules:

- Use names as specific as you can to avoid collisions.
- Use generic names for abstract interfaces.
- Prefer large meaningfully names to abbreviations.
    - If you use abbreviations anyway, use only very well known ones and use them **CONSISTENTLY**
- Avoid underscores but for constant and enum names
- Use `namespace` to avoid names collisions.
- Use **self-descriptive**, **pronounceable** names for **everything**.
- **BE CONSISTENT**. If something is named in a way do not use another name!
Example: If something is a `name` it should be a name everywhere, not an `id` or anything else.

<a id="NamingConvention:Variables"></a>
### Variables

- Begin with lowercase letter.
- Use [CamelCase](http://en.wikipedia.org/wiki/CamelCase)
- Use scope prefixes:
    - `m_` for object member variables.
    - `s_` for class member variables. ( `static` ones )

### Constants

- (%alternative%) Use uppercase letters. Separate words with *underscores*. Example: MY_CONSTANT
- (%alternative%) Use [variable-like names](#NamingConvention:Variables) but use "K" as the first character. Example: kMyConstant

### Methods and Functions

- Begin with uppercase.
- Use [CamelCase](http://en.wikipedia.org/wiki/CamelCase)

### class / struct

- Begin with uppercase.
- Use [CamelCase](http://en.wikipedia.org/wiki/CamelCase)

### Interfaces

- Begin with "I".
- Use [CamelCase](http://en.wikipedia.org/wiki/CamelCase)
- Use verbs and behaivoural words as names.

## Classes

##### Item: State explicit use of `virtual` keyword for virtual methods in hierarchy.
This way anyone looking at your class will be able to see clearly which methods are inherited from a baseclass or an interface and can be override. 

##### Item: Make data members private.
Do not use public nor protected data members, if you **really** need them to be accessed from outside the class ... think again and change your design.
If you need to access them anyway, create accessors. 

Anytime you create an accessor you are exposing your implementation and so breaking one of the OOP principles: Encapsulation.
To change this try to think in terms of sending messages to an object instead of calling methods, try to "tell " the object what it is happenning around and let them act in consecuence, because no one knows how they have to  react to an event better than them.

##### Item: Do not create [*passive* classes](http://cdjcpp.blogspot.com.es/2012/02/passive-and-active-classes.html)...
... Unless you need some kind of *data holder* ( which are merely convenient groupings of data and are not intended to encapsulate anything)
Think about objects methods as "message handlers" : When an object receive a message or event, What it has to do?

### Operator definitions.

##### Item: If needed, declare **both** comparison operators, and do it **consistently**.
When two operators are opposite overload both or none of them.

Example: 

*File MyClass.h*

    class MyClass
    {
    public:
        MyClass(void);
        virtual ~MyClass(void);
        bool operator==(const MyClass& ai_rhs) const;
        bool operator!=(const MyClass& ai_rhs) const;
    protected:
    private:
        uint32_t m_value;
    };

*File MyClass-inl.h*

    inline bool MyClass::operator==(const MyClass& ai_rhs) const
    {
        return ( m_value == ai_rhs.m_value);
    }
    inline bool MyClass::operator!=(const MyClass& ai_rhs) const
    {
       return !( ai_rhs == *this); 
    } 

##### Item: Protect assignment operators.
Use swap semantics when possible

Example:
    Foo& Foo::operator= (const Foo& foo)
    {
        Foo tmp(foo);
        swap(tmp);
        return *this;
    }  


##### Item: Do **NOT** overload operator&&, operator|| or operator, unless you have a VERY IMPORTANT reason
@todo: jlom Justificar


# Best Practices

## General
##### Item: Avoid long methods. Avoid deep nesting
##### Item: Do not use static objects in constructors
##### Item: Avoid type casting
##### Item: Use static class-scoped const instead of #define constants.
##### Item: Use enum instead of a bunch of constants
##### Item: Use inline methods instead of function macros
##### Item: Do not use goto
##### Item: Avoid magic numbers!
##### Item: Avoid using arrays as local variables or object fields
Aside  from questions of stack size, arrays used as local variables or object fields must have their bounds determined at compile time.
If you use large arrays with fixed bounds, consider whether your code is general enough.
If you are tempted to think,   

    “Who would ever  have more  than 100 elements  in  this  array?”

please remember a similar query: 

    “Who would ever want more than 64K  (or 640K!) of memory in a personal computer?” 

On the other hand, if the size of your array is derived from the log of the number of elements you deal with (because, for example, it is a stack for a recursive algorithm) and it has 100 elements in it, you are probably safe

##### Item: Use local variables on stack instead of heap.
##### Item: Prefer initialization list on constructors
##### Item: Compile cleanly at the highest warning level.
##### Item: Do not use goto ( yes again )
##### Item: Encapsulate global variables, constants, enumerated types and typedefs inside a class

## Design
##### Item: Rely on types, not on representations. (DO NOT TRY TO X-RAY OBJECTS)
##### Item: Prefer minimal classes to monolithic ones.
##### Item: One class one responsability
##### Item: Do NOT give away your internals
##### Item: Avoid inherit from classes that were not designed to be base classes
##### Item: Avoid type switching, prefer polymorphism
##### Item: Prefer composition over inheritance
##### Item: Inherit not to reuse, but to be reused.
##### Item: Provide abstract interfaces. Design for interfaces not for implementations.

## Memory and Resource Management
##### Item: Allocate storage only if you must
##### Item: Avoid using malloc and free. If you must do it be consistent
##### Item: Do NOT use memcpy and memcmp to copy/compare anything more structured than a raw memory
##### Item: Always provide empty branches for deleting array objects
##### Item: Postpone variable definition as long as posible
##### Item: Always assign a NULL value (0) to a deallocated pointer.
##### Item: Avoid allocating and deallocating memory in different modules
##### Item: Use RAII idiom when possible ( Resource Acquisition IS Initialization) @todo:jlom Link

## Methods
### Return types and values
##### Item: State return types for methods explicitly
##### Item: A public method MUST NEVER return a NON-CONST reference or pointer to member data.
##### Item: NEVER return a pointer or reference to a local varibale.
##### Item: Minimize the number of temporary objects created as return values

### Arguments
##### Item: State argument names explicitly in declarations
##### Item: Use references for arguments instead of pointers
##### Item: Limit default arguments
##### Item: Avoid methods with too many arguments
    They are dificult to maintain, to use , to read and to reuse. Think that your design is not good enough
##### Item: Use array arguments instead of pointers
##### Item: Use argument passing modes to document the intention
##### Item: Prefer references to pointers
##### Item: Use const references for input parameters and non-const references for output parameters
##### Item: If you have no other choice but to pass pointers as input parameters use `type const * const` construction.
*Tip*: Readed from right to left this:

    uint32_t const * const myVariable;

"myVariable is a const pointer to a const 32bits unsigned integer"


## Pointers and References
##### Item: DO NOT compare a potinter to NULL or assign NULL to a pointer. Use 0 instead
##### Item: Use references instead of pointers whenever possible
##### Item: Prefer references to pointer to pointer to pointer.
##### Item: If you have to use NULL use it **consistently**.
`NULL` is a define, so never assume that NULL valus is zero!

## [Const correcteness](http://www.parashift.com/c++-faq/const-correctness.html)
##### Item: Use const for methods that should not affect the state of the object
## Type Conversions
##### Item: When you have to make type cast USE C++ style cast.
Are easier to see, easier to search for and more explicit
##### Item: Avoid `reinterpret_cast` unless you have a **very good** reason

## Expressions
##### Item: Use break instead of boolean flags in loops. 
##### Item: Always use a default branch in switch statements 
##### Item: Use typedef for function pointers 
##### Item: Parenthesis are free ([as in free beer](http://en.wikipedia.org/wiki/Gratis_versus_libre#.22Free_beer.22_vs_.22free_speech.22_distinction)) . 
Use them to clarify the order of evaluation for operators in expressions and make them easier to read.  

Yes we know that you know by heart the [operator precedence in C++](http://en.cppreference.com/w/cpp/language/operator_precedence) but what if your colleague has had kryptonite for breakfast and you're mistaken?  
Even sometimes things gets [tough](http://stackoverflow.com/questions/5473107/operator-precedence-vs-order-of-evaluation)  
Remember our [hayku](#Zen)
##### Item: Prefer prefix increment/decrement to the postfix variant.
##### Item: Always have non-lvalues ( constant ones ) on the left side of a comparison.
This prevent undesired assignments inside comparisons
    
Example:This will lead to a really hard to find **error**
    
    uint32_t* data (packet->GetData());
    if( data = 0)
    {
        LogError_("Cannot get data from packet")
        return FAILURE;
    }

    // do whatever using data pointer

While this will raise an error in compile time    

    uint32_t* data (packet->GetData());
    if( 0 = data)
    {
        LogError_("Cannot get data from packet")
        return FAILURE;
    }

    // do whatever using data pointer



## Error Handling
##### Item: Prefer compile-time and link-time errors to run-time errors
##### Item: Assert liberally to document internal assumptions and invariants
##### Item: Do not let any error to pass silently.

## Variables
##### Item: USE initialization semantic instead of assigment.
##### Item: Variables are declared with the smallest possible scope.

## Namespaces
##### Item: Use namespaces to avoid name collisions
##### Item: Use namespaces consistently
##### Item: Do not use `using namespace` clauses.Prefer `alias` instead

## Virtuality
*note* most of the current data has been extracted from [this article][Virtuality]
##### Item: Prefer to make base class virtual functions private (or protected if you really must).

##### Item: Publicity vs. Privacy?
*"When should virtual functions be public, protected, or private?"*
The short answer is: Rarely if ever, sometimes, and by default, respectively - the same answer apply for other kinds of class members.  

The long answer:
We already know that all class members should be private unless we really need to expose them.

- Prefer to make interfaces nonvirtual, using [Template Method.][TemplateMethodPattern]
*Why is this such a good idea?*: We are used to write base classes using public virtual methods, this way we are specifying simultaneously interface and behaviour.  

    // Example 1: A traditional base class.
    class Widget
    {
    public:
    // Each of these functions might optionally be  
    // pure virtual,
        virtual int Process(Gadget&);  
        virtual bool IsDone(void);
    // ...
    }; 

The problem is that each virtual method is doing here two jobs ( and we all know this is not a god beguinning)
1. It is part of the public interface
2. It is specifying implementation details.

With this declaration derived classes can **replace** the base implementation at all.

What if we want to separate the interface from the implementation details? ( and we want for sure!)
We will end with some code that will remain you strongly of the [Template Method Pattern][TemplateMethodPattern], but this [idiom][CppIdioms] is more known as the [Non Virtual Interface][NonVirtualInterface]

    // Example 2: A more modern base class, using
    // Template Method to separate interface from
    // internals.
    class Widget
    {
    public:
    // Stable, nonvirtual interface.  
        int Process( Gadget& );    // uses DoProcess...()
        bool IsDone();             // uses DoIsDone()  
        // ...
    private:
    // Customization is an implementation detail that may
    // or may not directly correspond to the interface.
    // Each of these functions might optionally be  
    // pure virtual
        virtual int DoProcessPhase1( Gadget& );
        virtual int DoProcessPhase2( Gadget& );
        virtual bool DoIsDone();
    // ...
    };

This way we have a **stable interface** while still let the derived classes to customize the behaviour ( the main reason virtual methods were designed to.)
For example, notice that in Example 2 we've incidentally decided that it makes more sense for our users to see a single `Process()` function while allowing more flexible customization in two parts, `DoProcessPhase1()` and `DoProcessPhase2()`

*Beneficts*:
1. Base class is now in complete control of its interface and can enforce preconditions and postconditions, insert instrumentation, logging actions or any other similar work in one reusable place.
2. Now that we have separated interface and implementation we can make each of them take a different form without naturally. For example, notice that in Example 2 we've incidentally decided that it makes more sense for our users to see a single `Process()` function while allowing more flexible customization in two parts, `DoProcessPhase1()` and `DoProcessPhase2()`
3. The base class is now less fragile in the face of change. We are free to change our minds later and add pre- and postcondition checking, or separate processing into more steps, or refactor, or implement a fuller interface/implementation separation using the [Pimpl idiom][PimplIdiom]

*Inconvenients*:
1. Performance: "If our public method just call the private virtual one we have added a useless method call."
That is not really truth, most of the compilers of this century will optimize it away entirely.
2. Complexity: "More methods are needed" ... you have just to add one new method consisting in a call ....


Ok then, make virtual methods non-public but ... `protected` or `private`?  
Prefer to make virtual functions private... unless derived classes have a **really** good reason to call the base class version of the virtual method.



# Formatting

Aim for Readability!
Follow the W.O.R.M (Write Once Read Many) principle when writting code.

## Proposed style
- Use blank spaces instead of tabs for indentation ( **and configure your editor properly**)
- Use two (2) spaces to indent code.
- Use blank space after commands: while for switch ... )
- Use blank space after "," in argument list
- Brackets always start in a new line
- Brackets defining a block have to be always placed in the same colunm.
- Control primitives should be followed by a block even if it is empty.
- The derreference(*) operator and the address-of operator (&) should be directly connected ( no space ) with the type name in declarations and definitions
- Characters “*” and “&” should be written together with the types of varibles instead of with the names of variables to emphasize that they are part of the type definition.
- NEVER declare more than one variable in a single statement.
- Do not use space aroung “.” or “->” operators.
@todo: jlom Tengo un fichero de AStyle que automatiza la mayoria de estas cosas, y se puede integrar facilmente con vim y con emacs.


# Exceptions

##### Item: Always explicit which exceptions will throw your methods
Remember that if you do not expecify anything that menas a method can throw ANY exception

##### Item: Use "Resource Acquisition Is Initialization" idiom. 
[See][RAII] 


## Project Directory Structure

### Item number %item_numer%
### %Headline%
#### What
#### Why
#### Example:
[TAGS] : layout, comments, scope, best_practice
[Link](#CodeLayout)

Links:
[TemplateMethodPattern]: http://en.wikipedia.org/wiki/Template_method_pattern
[CppIdioms]: http://en.wikibooks.org/wiki/More_C%2B%2B_Idioms
[NonVirtualInterface]: http://en.wikibooks.org/wiki/More_C%2B%2B_Idioms/Non-Virtual_Interface
[Virtuality]: http://www.gotw.ca/publications/mill18.htm
[PimplIdiom]: http://en.wikibooks.org/wiki/C%2B%2B_Programming/Idioms#Pointer_To_Implementation_.28pImpl.29
[RAII]: http://en.wikipedia.org/wiki/Resource_Acquisition_Is_Initialization