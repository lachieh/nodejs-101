# Node.js

First, setup your project by running `npm init` and answering the questions. Make sure you add a `.gitignore` file and include `node_modules` in that file. Commit and push and you're good to get started. Read through all of the exercises and then attempt them in individual scripts.

## Small

### Read a file

Write a program that prompts the user to enter a file name, and reads in the contents of the file, convert the text to all caps, and prints it out.

Assuming the file file1.txt contains the text: Hello, I am file 1..

Example output:

```bash
$ node cap_file.js
filename: file1.txt
HELLO, I AM FILE 1.
```

Trigger an error condition by running the program on a non-existent file. Your program should display the error message, and it should display something like:

```bash
$ node cap_file.js
filename: blah.txt
ENOENT: no such file or directory, open 'blah.txt'
```

### DNS lookup

Write a program that prompts the user for a domain name, looks up the IP address for the domain, and prints it out.

Example:

```
   $ node dns_lookup.js
   Domain name: yahoo.com
   IP Address: 98.139.183.24
```

Trigger an error condition by providing an invalid domain.See that the error gets displayed.

### Read and write

Write a program to prompt the user for two file names, the first file will be the input and the second file will bethe output. The program will read in the contents of the input file, convert its text to all caps, and then write the resulting contents to the output file.

Example:

```bash
   $ node cap_file_2.js
   Input file: file1.txt
   Output file: output.txt
   Wrote to file output.txt
```

As a result, `output.txt` should now contain the text `HELLO, I AM FILE 1.`

Trigger an error by running the program with an non-existing input file, ensure that the error is properly displayed. Trigger an error by running the program with an output file in a non-existant directory, such as thisdirdoesntexist/output.txt, ensure that the error is properly displayed.

### Save a web page

Write a program to save a web page. Prompt the user for a URL for the web page he wants to save, and for the filename to save to. For example:

```
$ node save_web_page.js
URL: https://css-tricks.com/creating-book-cover-using-javascript-p5-js/
Save to file: cover-book.html
Saved to file cover-book.html
```

As result `cover-book.html` should have the HTML source code from the entered URL.

- Trigger an error by running the program with an invalid URL, ensure the error is properly displayed.
- Trigger an error by running the program with an output file in a non-existent directory, such as `thisdirdoesntexist/output.txt`, ensure that the error is properly displayed.

## Medium

### Resize an image

Write a program to download the JavaScript logo from https://raw.githubusercontent.com/voodootikigod/logo.js/master/js.png, and resize it using the gm module to the size 240x240. You might use the request module to download the file. Hint: You will set the encoding option to null for request. Example:
var options = {
url: 'http://example.com/example.png', encoding: null
};
request(options, function(err, response, imageData) {
// save image data and resize
});

## Large

### Combine All of the above exercises

Using all of the modules above, write a script that will:

- Asks the user for a domain name (i.e. google.com)
- Lookup the DNS info for the domain
- Save the DNS lookup to a new file
- Get the HTML for the homepage of the URL (https://google.com)
- Find the first image on the page (you might need to use regex for this.)
- Resize the image
- Save the image to a file
