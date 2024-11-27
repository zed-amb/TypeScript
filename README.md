## Typescript Architecture
The below points are the most important features of the Typescript. They are:
1. TypeScript Core Compiler

    core.ts        It checks the code structure and keywords.
    program.ts    It checks the syntax and services.
    scanner.ts        It handles input.
    emitter.ts        It handles output.
    checker.ts        It verifies the data structure.
    parser.ts        It handles data conversion.
 
    - It checks syntax errors, keywords and program structure.
    - It reports the issues in program.
   
2. Standalone TS Compiler

    tsc.ts        It trans complies the Typescript code into JavaScript

3. Language Service

    services.ts    It provides values and functions required for TS language.
            TS complier uses services to verify the code.

4. TS Server

    server.ts        It hosts the TS application and handles request & response.

5. VS Shim

    shims.ts        It makes TypeScript language cross platform.


6. VS Managed Language    It refers to managed code.
    Service            Managed code is the code understandable to all OS services.


Install TypeScript on your PC:

1. Open Command Prompt

2. Run the command

    C:\> npm install  -g  typescript  

3. Check the version

    C:\> tsc  -v

4. Create a new folder for Typescript project

    D:\ts-project

5. Open folder in VS code and run the following commands

    >npm init -y
    >tsc  -init
     - tsc  generates  "tsconfig.json", which is typescript configuration file for language and file system.
     - TypeScript rules are defined using tsconfig.json

6. TypeScript program is written in a file with extention ".ts"

        index.ts

7. You have to transcompile the typescript into javacript

    > tsc  index.ts
       [It will generate a new file by name index.js]

8. You can embed into HTML page or run using node compliler.

    > node  index.js

                 TypeScript Language
1. Variables
- Variables are declared by using var, let, const.
- Variable is configured with data type.

    var  variableName : dataType  = value;
   
    var  price:number = 10000;
    var  name:string  = "TV";

- The data types are JavaScript types

    a) Primitive Types
    b) Non Primitive Type

- Primitive Types
    number, string, boolean, null, undefined, symbol, bigint

- If data type is not defined for variable then it is by default "any" type.
- "any" is the root for all data types.

    var price;            // price is any type     var price:any;

- TypeScript support "Type Inference", the data type is defined according to the value initialized.

    var price = 4000;        // price is number
    price = "TV";        // invalid
   
    var price;            // any
    price = 4000;        // valid
    price = "TV";        // valid
    price = true;        // valid

Syntax:
    let  price:number;
    let  name:string;
    let  stock:boolean;

    price = 5000.55;
    name = "TV";
    stock = true;

- TypeScript supports Union of types.
- You can configure multiple types for a variable.

    let  variableName: dataType1 | dataType2 | ...  ;

    let  name: string | null = prompt();
    let  flag: boolean = confirm();

Ex:
    let  val : string | number | boolean;

    val = "TV";
    val = 5000;
    val = true;
    val = null;        // invalid


                Non Primitive Types

1. Array in TypeScript
- Array declaration requires type specification.

    var  values : string[];
    var  values : number[];
    var  values : any[];

- Typescript can restrict array to values of similar data type.
- It also allows to configure array that can handle various types of values, which is known as
  "Tuple".
- Array declaration requires memory allocation, which you can do by using
    a) Array() constructor
    b) [ ] meta character

Syntax:
    let values:string[]  = [ ];        static memory
    let values:string[] = new Array();    dynamic memory
