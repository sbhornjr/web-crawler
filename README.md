# web-crawler

I took this project step by step - I first read the linked HTTP tutorial to
learn the basic concepts and syntax. Then I started the coding by creating a
socket and connecting to the server, then sending the first GET request on the
login page. Once I got that, I realized that I was going to need a way to parse
HTTP to get things like cookies and response codes, I created an HTTPParser
class with various such functions. It took me a little while to get logged in
to fakebook with HTTP 1.0, so I decided to switch to 1.1 and it somehow worked
instantly. Once I was logged in successfully, I created the while loop that would
run through links that I see and feed them to the HTMLParser. My HTMLParser class
inherits from the HTMLParser.HTMLParser class. I overrode a couple of functions
so that when I feed into it, it does things such as looks for links and looks
for secret flags automatically. So, all I had to do was feed each page into the
parser and the flags were found. My biggest challenges were connecting at first
(it took me a while to decide to try in HTML 1.1) and dealing with chunking.