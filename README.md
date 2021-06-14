#Naming Conventions

In general, code is written once but read multiple times, by others in
the project team or even those from other teams. Readability is
therefore important. Readability is nothing more than figuring out what
the code does in less time.

Among the many best practices of coding, is the way variables,
functions, classes and even files are named in a project. A common
naming convention that everyone agrees to follow must be accompanied by
consistent usage. This will result in developers, reviewers and project
managers communicate effectively with respect to what the code does.

While there are well-established naming conventions, there\'s no single
one that fits all scenarios. Each programming language recommends its
own convention. Each project or organization may define its own
convention.

Category of Naming Conventions
------------------------------

It\'s common to categorize a naming convention as one of these:

-   Typographical: This relates to the use of letter case and symbols
    such as underscore, dot and hyphen.

-   Grammatical: This relates to the semantics or the purpose. For
    example, classes should be nouns or noun phrases to identify the
    entity; methods and functions should be verbs or verb phrases to
    identify action performed; annotations can be any part of
    speech; interfaces should be adjectives.

Grammatical conventions are less important for variable names or
instance properties. They are more important for classes, interfaces and
methods that are often exposed as APIs.

Typical Scope of Naming Conventions
-----------------------------------

Naming convention is applicable to constants, variables, functions,
modules, packages and files. In object-oriented languages, it\'s
applicable to classes, objects, methods and instance variables.

Naming Conventions Advantages
-----------------------------

Naming conventions are probably not important if the code is written by
a single developer, who\'s also the sole maintainer. However, typical
real-world projects are developed and maintained by teams of developers.
Particularly in the context of open source projects, code is shared,
updated and merged by many individuals across organizations and
geographies. Naming conventions are therefore important.

Naming conventions lead to predictability and discoverability. A common
naming convention, coupled with a consistent project structure, makes it
easier to find files in a project.

Naming Conventions Type
-----------------------

In this document, we will explain more about naming conventions for:

-   Database Naming Conventions

-   Coding Naming Conventions

### Database Naming Conventions

There are two key elements to any software experience: the application
and the data. Both elements need to be present for a functional end-user
experience.

The application component is stateless, so the teams can simply
overwrite the application with the latest version when releasing new
software experiences. However, unlike the application, the database
component cannot simply be overwritten. Data is a persistent and
valuable resource. Unlike applications, databases are stately. As a
result, the database is one of the most valuable and important assets to
the organization -- therefore database version control is needed.

Database versioning begins with database schema, or the structure of the
database. In order to effectively version a database, you need to track
and understand the changes that are happening.

Things to consider:

-   Identifiers should be written entirely in lower case. This includes
    tables, views, column, and everything else too. Mixed case
    identifier names means that every usage of the identifier will need
    to be quoted in double quotes. Example: use first_name not
    "First_name".

-   Data types are not names. Database object names, particularly column
    names, should be a noun describing the field or object. Avoid using
    words that are just data types such as text or timestamp

-   Underscores separate words. Object name that are comprised of
    multiple words should be separated by underscores.

Example: word_count or team_member_id, not wordcount or wordCount.

-   Full words, not abbreviations. Object names should be full English
    words. In general, to avoid abbreviations. Example: use middle_name
    not mid_nm.

-   Tables, views, and other relations that hold data should have
    singular names, not plural. This means our tables and views would be
    name team, not teams

-   The sentences are consistency and unambiguous.

-   Single column primary key fields should be named "id"

-   Foreign key fields should be a combination of the name of the
    referenced table and the name of the referenced fields.

-   Object names should not include the object types of them.

-   All modern databases support some form of namespacing. For example,
    in postgresql you can create schemas to group database objects. If
    you have multiple applications sharing the same database and want to
    prevent them from clobbering each other, use schemas instead.

-   Some database commands that create database objects do not require
    you specify a name. You should be explicitly specifying names.

-   Indexes should be explicitly names and include both the table name
    and the column name(s) indexed.

-   Similar to indexes, constraints should give descriptive names. This
    is especially true for check constraints. It's much easier to
    diagnose an errant insert if the check constraints that was violated
    lets you know the cause.

### Coding Naming Conventions

Coding naming conventions is a rule to follow as you decide what to name
your identifiers such as class, package, variable, constant, method,
etc. By using this standard, make your code easier to read for yourself
and other programmers.

The following are the key rules that must be followed by every
identifier:

-   The name must not contain any white spaces.

-   The name should not start with special characters like &
    (ampersand), \$ (dollar), \_ (underscore).

-   Consistency names in classes, objects, methods, and instance
    variables.

-   In general, use nouns for classes, verbs for functions, and names
    that show purpose for variables, attributes and arguments.

-   Separators objections:

    a.  With Camel Case and Pascal Case, there are no word separators.
        Readability is achieved by capitalizing the first letter of each
        word. Language adopting: Pascal, Modula, Java, and .NET.

    b.  With Snake Case, underscore is the separator. This practice is
        common in Python, Ruby, C/C++ standard libraries, and WordPress.

    c.  With Kebab Case, hyphen is the separator. Language adopting:
        COBOL, Lisp, Perl 6, and CSS. Since hyphen in many languages is
        used for subtraction, Kebab Case is less common than Snake Case.

```{=html}
<!-- -->
```
-   Things to consider:

a.  Reveal intentions: fileName is better f; maxPugs is better than
    pugs.

b.  Make distinctions; moneyInDollars is better than money.

c.  Put the distinguishing aspect first: dollarMoney and rupeeMoney are
    better than moneyInDollars and moneyInRupees.

d.  Easy to pronounce: timeStamp is better than ts.

e.  Verbs for functions: getName() and isPosted() are
    good; hasWeight() or isMale() when boolean values are
    returned; toDollars() for conversions.

f.  One word, one concept: fetch, retrieve, get all imply the same
    thing: use one of them consistently.

g.  Relate to business context: AddCustomer is better
    than IncrementCounter.

h.  Use shortforms judiciously: PremiumCust may be used
    over PremiumCustomer to emphasize \"Premium\"; but fn is not a good
    substitute for fileName.

i.  Describe content rather than storage: user_info is better
    than user_list.

j.  Plurals for containers: fruitNames is better than fruit for an array
    of fruit names.
