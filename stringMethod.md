Give a short description of what the method does, how it works, it's time complexity (if appropriate), and give three examples of it in action!

Please research the following string methods:



charAt:
    - Definition: 
        - returns a new string consisting of the single UTF-16 code unit located at the specified offset into the string.
    - Syntax : 
        - charAt(index)
    -Parameters:
        - index: An integer between 0 and str.length - 1. If the index cannot be converted to the integer or no index is provided, the default is 0, so the first character of str is returned.
    -Examples
        - 1
            - const sentence = 'The quick brown fox jumps over the lazy dog.';

            - const index = 4;

            - console.log(`The character at index ${index} is ${sentence.charAt(index)}`);
            -// expected output: "The character at index 4 is q"
        - 2
            - var anyString = 'Brave new world';

            - console.log("The character at index 0   is '" + anyString.charAt(0)   + "'");

            - The character at index 0   is 'B'
        - 3


charCodeAt
    - Definition
        -  method returns an integer between 0 and 65535 representing the UTF-16 code unit at the given index. The UTF-16 code unit matches the Unicode code point for code points which can be represented in a single UTF-16 code unit. If the Unicode code point cannot be represented in a single UTF-16 code unit (because its value is greater than 0xFFFF) then the code unit returned will be the first part of a surrogate pair for the code point.
    - Syntax
        - charCodeAt(index)
    - Parameters
        - An integer greater than or equal to 0 and less than the length of the string. If index is not a number, it defaults to 0.
    - Examples
        - 1
            - const sentence = 'The quick brown fox jumps over the lazy dog.';

            - const index = 4;

            - console.log(`The character code ${sentence.charCodeAt(index)} is equal to ${sentence.charAt(index)}`);
            
            - // expected output: "The character code 113 is equal to q"
        - 2
            - 'ABC'.charCodeAt(0)  // returns 65

concat
    - Definition
        -  concatenates the string arguments to the calling string and returns a new string.
    - Syntax
        -  concat(str1)
        -  concat(str1, str2)
        -  concat(str1, str2, ... , strN)
    - Parameters
        -  One or more strings to concatenate to str.
    - Examples
        - 1
            - const str1 = 'Hello';
            - const str2 = 'World';
                - console.log(str1.concat(' ', str2));
                    - // expected output: "Hello World"
                - console.log(str2.concat(', ', str1));
                    - // expected output: "World, Hello"
        - 2
            - let hello = 'Hello, '
                - console.log(hello.concat('Kevin', '. Have a nice day.'))
                    - // Hello, Kevin. Have a nice day.

includes
    - Definition
        - performs a case-sensitive search to determine whether one string may be found within another string, returning true or false as appropriate.
    - Syntax
        - includes(searchString)
        - includes(searchString, position)
    - Parameters
        - searchString
            - A string to be searched for within str
        - position //optional
            - The position within the string at which to begin searching for searchString. (Defaults to 0.)
    - Return value
        - true if the search string is found anywhere within the given string; otherwise, false if not.
    - Examples
        - 1
            - const sentence = 'The quick brown fox jumps over the lazy dog.';

            - const word = 'fox';

            - console.log(`The word "${word}" ${sentence.includes(word) ? 'is' : 'is not'} in the sentence`);
                -   // expected output: "The word "fox" is in the sentence"
        - 2
            - const str = 'To be, or not to be, that is the question.'
                - console.log(str.includes('To be'))        // true

indexOf
    - Definition
        - returns the index within the calling String object of the first occurrence of the specified value, starting the search at fromIndex. Returns -1 if the value is not found.
    - Syntax
        - indexOf(searchValue)
        - indexOf(searchValue, fromIndex)
    - Parameters
        - searchValue
            - The string value to search for.
            - If no string is explicitly provided, searchValue will be coerced to "undefined", and this value will be searched for in str.
        - fromIndex
            - An integer representing the index at which to start the search. Defaults to 0.
    - Examples
        - 1
            - const paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

            - const searchTerm = 'dog';

            - const indexOfFirst = paragraph.indexOf(searchTerm);

            - console.log(`The index of the first "${searchTerm}" from the beginning is ${indexOfFirst}`);
            
            - // expected output: "The index of the first "dog" from the beginning is 40"
        - 2
            - const str = 'Brave new world'

            - console.log('Index of first w from start is ' + str.indexOf('w'))   // logs 8

            - console.log('Index of "new" from start is ' + str.indexOf('new'))   // logs 6


match
    - Definition
        - retrieves the result of matching a string against a regular expression (regex).
    - Syntax
        - match(regexp)
    - Parameters
        - regexp
            - A regular expression object.
            - If regexp is a non-RegExp object, it is implicitly converted to a RegExp by using new RegExp(regexp).
            - If you don't give any parameter and use the match() method directly, you will get an Array with an empty string: [""].
    - Examples
        - 1 
            - const paragraph = 'The quick brown fox jumps over the lazy dog. It barked.';

            - const regex = /[A-Z]/g;

            - const found = paragraph.match(regex);

            - console.log(found);
                - // expected output: Array ["T", "I"]

        - 2
            -  const str = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz';

            - const regexp = /[A-E]/gi;

            - const matches_array = str.match(regexp);

            - console.log(matches_array);
                - // ['A', 'B', 'C', 'D', 'E', 'a', 'b', 'c', 'd', 'e']

repeat
    - Definition
        - constructs and returns a new string which contains the specified number of copies of the string on which it was called, concatenated together.
    - Syntax
        - repeat(count)
    - Parameters
        - count
            - An integer between 0 and +Infinity, indicating the number of times to repeat the string.
    - Examples
        - 1
            - const chorus = 'Because I\'m happy. ';

            - console.log(`Chorus lyrics for "Happy": ${chorus.repeat(27)}`);

                - // expected output: "Chorus lyrics for "Happy": Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. "
        - 2 
            - 'abc'.repeat(2)  
                - 'abc'.repeat(2)     // 'abcabc'


replace
    - Definition
        - returns a new string with some or all matches of a pattern replaced by a replacement. The pattern can be a string or a RegExp, and the replacement can be a string or a function to be called for each match. If pattern is a string, only the first occurrence will be replaced.
    - Syntax
        - replace(regexp, newSubstr)
        - replace(regexp, replacerFunction)

        - replace(substr, newSubstr)
        - replace(substr, replacerFunction)
    - Parameters
        - regexp (pattern)
            - A RegExp object or literal. The match or matches are replaced with newSubstr or the value returned by the specified replacerFunction.
        - substr
            - A String that is to be replaced by newSubstr. It is treated as a literal string and is not interpreted as a regular expression. Only the first occurrence will be replaced.
        - newSubstr
            - The String that replaces the substring specified by the specified regexp or substr parameter. A number of special replacement patterns are supported; see the "Specifying a string as a parameter" section below.
        - replacerFunction
            - A function to be invoked to create the new substring to be used to replace the matches to the given regexp or substr. 
    - Examples
        - 1 
            - const p = 'The quick brown fox jumps over the lazy dog. If the dog reacted, was it really lazy?';
            - console.log(p.replace('dog', 'monkey'));
            - // expected output: "The quick brown fox jumps over the lazy monkey. If the dog reacted, was it really lazy?"
        - 2 
            - const p = 'The quick brown fox jumps over the lazy dog. If the dog reacted, was it really lazy?';
            - const regex = /Dog/i;
            - console.log(p.replace(regex, 'ferret'));
            - // expected output: "The quick brown fox jumps over the lazy ferret. If the dog reacted, was it really lazy?"



search
    - Definition
        - method executes a search for a match between a regular expression and this String object.
    - Syntax
        - search(regexp)
    - Parameters
        - regexp
            - a regular expression object
    - Examples
        - 1
            - const paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';
            - const regex = /[^\w\s]/g; // any character that is not a word character or whitespace
            - console.log(paragraph.search(regex));
            - // expected output: 43
        - 2 
            - let str = "hey JudE"
            - let re = /[A-Z]/g
            - console.log(str.search(re))    // returns 4, which is the index of the first capital letter "J"


slice
    - Definition
        - method extracts a section of a string and returns it as a new string, without modifying the original string.
    - Syntax
        - slice(beginIndex)
        - slice(beginIndex, endIndex)
    - Parameters
        - beginIndex
            - The zero-based index at which to begin extraction. If negative, it is treated as str.length + beginIndex. (For example, if beginIndex is -3, it is treated as str.length - 3.) If beginIndex is not a number after Number(beginIndex), it is treated as 0
        - endIndex
            - The zero-based index before which to end extraction. The character at this index will not be included.
            - If endIndex is omitted or undefined, or greater than str.length, slice() extracts to the end of the string. If negative, it is treated as str.length + endIndex.
    - Examples
        - 1
            - const str = 'The quick brown fox jumps over the lazy dog.';
            - console.log(str.slice(31));
                - // expected output: "the lazy dog."
        - 2
            - const str = 'The quick brown fox jumps over the lazy dog.';
            - console.log(str.slice(4, 19));
                - // expected output: "quick brown fox"
        - 3
            - const str = 'The quick brown fox jumps over the lazy dog.';
            - console.log(str.slice(-4));
                - // expected output: "dog."

split
    - Definition
        - divides a String into an ordered list of substrings, puts these substrings into an array, and returns the array.  The division is done by searching for a pattern; where the pattern is provided as the first parameter in the method's call.  
    - Syntax
        - split()
        - split(separator)
        - split(separator, limit)
    - Parameters
        - separator
            - The pattern describing where each split should occur.  The separator can be a simple string or it can be a regular expression.
        - limit
            - A non-negative integer specifying a limit on the number of substrings to be included in the array. If provided, splits the string at each occurrence of the specified separator, but stops when limit entries have been placed in the array. Any leftover text is not included in the array at all.
    - Examples
        - 1
            - const str = 'The quick brown fox jumps over the lazy dog.';
            - const words = str.split(' ');
            - console.log(words[3]);
                - // expected output: "fox"
        - 2
            - const str = 'The quick brown fox jumps over the lazy dog.';
            - const chars = str.split('');
            - console.log(chars[8]);
                - // expected output: "k"
        - 3
            - const str = 'The quick brown fox jumps over the lazy dog.';
            - const strCopy = str.split();
            - console.log(strCopy);
                - // expected output: Array ["The quick brown fox jumps over the lazy dog."]


substr
    - Definition
        - returns a portion of the string, starting at the specified index and extending for a given number of characters afterwards.
    - Syntax
        - substr(start)
        - substr(start, length)
    - Parameters
        - start
            - The index of the first character to include in the returned substring.
        - length
            - Optional. The number of characters to extract.
    - Examples
        - 1
            - const str = 'Mozilla';
            - console.log(str.substr(1, 2));
                - // expected output: "oz"
        - 2
            - const str = 'Mozilla';
            - console.log(str.substr(2));
                - // expected output: "zilla"

toLowerCase
    - Definition
        - returns the calling string value converted to lower case.
    - Syntax
        - toLowerCase()
    - Parameters
    - Examples
        - 1 
            - const sentence = 'The quick brown fox jumps over the lazy dog.';
            - console.log(sentence.toLowerCase());
            - // expected output: "the quick brown fox jumps over the lazy dog."


toUpperCase
    - Definition
        - returns the calling string value converted to uppercase (the value will be converted to a string if it isn't one).
    - Syntax
        toUpperCase()
    - Parameters
    - Examples
        - 1 
            - const sentence = 'The quick brown fox jumps over the lazy dog.';
            - console.log(sentence.toUpperCase());
                - // expected output: "THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG."
trim
    - Definition
        - removes whitespace from both ends of a string. Whitespace in this context is all the whitespace characters (space, tab, no-break space, etc.) and all the line terminator characters (LF, CR, etc.).
    - Syntax
        - trim()
    - Parameters
    - Examples
        - 1
            - const greeting = '   Hello world!   ';
            - console.log(greeting.trim());
                - // expected output: "Hello world!";
        - 2
            - var orig = '   foo  ';
            - console.log(orig.trim()); 
             - // 'foo'


