+++
Categories = ["Fundamentals"]
Description = "Using Integer Numbers"
Tags = []
author = "Owen"
concepts = ["Numbers"]
date = "2015-03-16T16:13:34Z"
keystage = ["KS2"]
subtitle = "and simple sums"
title = "Numbers"
featured = ["featured"]
slides = "numbers"
lessonplan = "numbers"
notesfor = "numbers"
keystagelevel = ["lower"]
lessonnumber = "1"
+++
### What we are going to learn
Computers are used to process data. All data is made up of numbers. Yes, really!
Everything is just a bunch of numbers to a computer. These are the only things
they understand.

We are going to explain how a numbers are used in Go programs. Then we are
going to show you how to do type sums in Go.

### Before you begin
Before we begin we are going to assume that you have Go installed and it is
working on our computer. If you have not installed Go yet then you need to read
our [Go install guide]({{< ref "installing-go.md" >}}). We are also assuming that you have
installed either Atom or LiteIDE of your computer. Again if you have not done
this yet you need to go and read our [editor install
guide](/installing-go/#editor-install).

Once you have Go installed it is time to start.

### Everything is a Number

Computers process data, that's their job. But they only process one type of
data - numbers. Everything, and we mean __everything__ is just a bunch of
numbers to a computer. You might thing a picture is a picture or a word is a
word but not to a computer. They are all numbers.

{{% panelInfoTitle title="Now it is your turn" %}}
Rainbows are made up of seven colours

* Red
* Orange
* Yellow
* Green
* Blue
* Indigo
* Violet

How could you represent these as numbers?

{{% expandingButton id="rainbow-answers" name="Answer" %}}
You have to pick a number to each colour. For example

* Red = 1
* Yellow = 2
* Orange = 3
* Green = 4
* Blue = 5
* Indigo = 6
* Violet = 7

Now the sequence

7, 6, 5, 4, 1, 2, 3 means

Violet, Indigo, Blue, Green, Red, Yellow, Orange

This is similar to what the computer does with colours. The computer just just
uses much bigger numbers to represent lots more colours.
{{% /expandingButton %}}
{{% /panelInfoTitle %}}

### Starting small
Go programs are programmed by typing. You type Go commands into your text
editor and save the file as a Go __source code__ file. That's a file with a
`.go` file extension, like the `helloworld.go` that we saw when you tested your Go installation.

This is a different process compared to programming in [Scratch](https://scratch.mit.edu/). You program in Scratch by joining coloured
blocks together instead of typing commands. But this is not what professional
programmers do, we type instructions.

We are going to use Go to teach you what is inside the coloured blocks that
Scratch uses.

Starting with numbers.

### Numbers in Go
We are going to start with whole numbers. These are numbers you use when you
count like 1, 2, 3, 10, 50 or 100 and 0. Go calls these numbers __integer__ numbers, or `int` for short. You can use numbers in Go the same way you use
them at school. You can add them, subtract them, multiply them and divide them.

### Sums in Go
Typing sums in Go is easy. It is almost the same as you are used to.

Addition is typed with a `+` typed <kbd>Shift</kbd>+<kbd>=</kbd> like this `1 + 2`

Subtraction is typed with a `-` like this `6 - 3`

Multiplication is a little harder. You cannot type a &#215;, instead you have to
type a `*` typed <kbd>Shift</kbd>+<kbd>8</kbd> for multiplication like this `4 * 3`

Division is a similar to multiplication. You cannot type a &#247;, instead you have
to type a `/` like this `10 / 2`

{{% panelInfoTitle title="Now it is your turn" %}}
Can you work out the answers to these sums?

{{< hilight lang="txt" style="edit-gedit" lineNumbers="y" >}}
4 + 5 = ??

7 - 3 = ??

4 * 8 = ??

16 / 4 = ??
{{< /hilight >}}
{{% expandingButton id="rainbow-answers" name="Answer" %}}
The answers are
{{< hilight lang="txt" style="edit-gedit" lineNumbers="y" >}}
4 + 5 = 9

7 - 3 = 4

4 * 8 = 32

16 / 4 = 4
{{< /hilight >}}
{{% /expandingButton %}}
{{% /panelInfoTitle %}}

### The Numbers Program

Let's write a Go program to show you this.

Open your terminal or command prompt.
We are going to put each Go program in its own directory. This is the recommended
practice for Go programs.
In your terminal you need to change to the location of your Go Workspace.
To do this type

{{% panelPrimaryTitle title="On Linux, Raspberry Pi and Mac OS X" %}}
{{< hilight lang="sh" style="neon" lineNumbers="n" >}}
cd $GOPATH/src/
{{< /hilight >}}
{{% /panelPrimaryTitle %}}

{{% panelSuccessTitle title="On Windows" %}}
{{< hilight lang="sh" style="neon" lineNumbers="n" >}}
cd %GOPATH%\src\
{{< /hilight >}}
{{% /panelSuccessTitle %}}

Now you need to make a new directory. We need to call this `numbers` after the
program we will write. Then we need to change directory into the new new `numbers`
directory.

{{< hilight lang="sh" style="neon" lineNumbers="n" >}}
mkdir numbers
cd numbers
{{< /hilight >}}

Now you need to start you editor, either Atom or LiteIDE

{{% panelPrimaryTitle title="On Linux, Windows and MacOS X" %}}
{{< hilight lang="sh" style="neon" lineNumbers="n" >}}
atom numbers.go
{{< /hilight >}}
{{% /panelPrimaryTitle %}}

{{% panelSuccessTitle title="On Raspberry Pi" %}}
{{< hilight lang="sh" style="neon" lineNumbers="n" >}}
liteide numbers.go
{{< /hilight >}}
{{% /panelSuccessTitle %}}

The `numbers.go` tells Atom or liteIDE start with the file `number.go` open in
the editor. If the file does not exist the editor will create it for you.

Once you editor starts you can type in the `numbers.go` program.

{{% panelWarningTitle title="Type carefully" %}}
Remember to type in `numbers.go` exactly as we have it here.
{{% /panelWarningTitle %}}

{{% codeFigure caption="Fig-1. The `numbers.go` code" %}}
{{< hilight lang="go" style="edit-gedit" lineNumbers="y" >}}
package main

import "fmt"

func main() {
	fmt.Println("The numbers program shows you how to add, subtract")
	fmt.Println("multiple and divide integer numbers.")
	fmt.Println("One plus one is typed: 1+1")
	fmt.Print("1+1=")
	fmt.Println(1 + 1)

	fmt.Println("Ten subtract three is typed: 10-3")
	fmt.Print("10-3=")
	fmt.Println(10 - 3)

	fmt.Println("Three multiplied by four is typed: 3*4")
	fmt.Print("3*4=")
	fmt.Println(3 * 4)

	fmt.Println("Six divided by two is typed: 6/2")
	fmt.Print("6/2=")
	fmt.Println(6 / 2)
}
{{< /hilight >}}
{{% /codeFigure %}}

Once you have typed the program in, you need to save it. Once you have saved it
you need to run it with:

{{< hilight lang="sh" style="neon" lineNumbers="n" >}}
go run numbers.go
{{< /hilight >}}

If you typed the program correctly you should see

{{< hilight lang="txt" style="edit-gedit" lineNumbers="n" >}}
The numbers program shows you how to add, subtract
multiple and divide integer numbers.
One plus one is typed: 1+1
1+1=2
Ten subtract three is typed: 10-3
10-3=7
Three multiplied by four is typed: 3*4
3*4=12
Six divided by two is typed: 6/2
6/2=3
{{< /hilight >}}

The important parts of the program are lines 9 and 10, and the similar lines 13
and 14, 17 and 18, and 21 and 22.

Lines 6, 7 and 8 use the `Println` function from the `fmt` (short for format)
package to print what is between the "'s. You have used this function before
when you wrote Hello World to test your Go install.

Line 9 is very similar to the `Println` function used in line 8. The `Print`
function from the `fmt` also prints what is between the "'s but does not take a
new line at the end.

Line 10 is the key line. Let us look at it more closely.

{{% codeFigure caption="Fig-2. Line 10 from `numbers.go`" %}}
{{< hilight lang="go" style="edit-gedit" lineNumbers="n" >}}
	fmt.Println(1 + 1)
{{< /hilight >}}
{{% /codeFigure %}}

The first part of line 10 used the `Println` function from the `fmt` package.
The question you now need to ask is what will this print? The answer is as
simple as `2`.

The next question to ask is why is it `2`? OK, well it is `2` because that
is the answer you would expect if you added one and one together.

But why does it not print `1+1`? Well, in simple terms it is because the `1+1`
is not inside "'s. We will see why this is important when we talk about words.

So what happens then? When you run the program the computer sees the
`fmt.Println` and knows that you want to print something to the terminal
window.
But at this point it does not what you want to print. To work that out it looks
at what is inside the brackets, the `(...)`.

Inside the brackets it sees `1+1`. The computer has not seen any "'s so it
knows that it cannot print this. But because there are no "'s computer knows
that it has to work out the answer to `1+1` and then print the answer.

Which is why you see a `2`

If we look at the output

{{% codeFigure caption="Fig-3. The output of lines 9 and 10 from `numbers.go`" %}}
{{< hilight lang="go" style="edit-gedit" lineNumbers="n" >}}
1          +            1     =            2
|<---- line 9 prints this ---->|<---- line 10 prints this ---->|
{{< /hilight >}}
{{% /codeFigure %}}

line 9 prints the first part, which is everything to up to and including the
equals sign. Then line 10 prints the answer, which is 2, on the end and then
takes a new line.

Now you know how the program works we can explain the bit at the
start of the program. These are lines 1 and line 5

{{< hilight lang="go" style="edit-gedit" lineNumbers="n" >}}
package main
....
func main() {
{{< /hilight >}}

These come as a pair. Line 1 declares that this file is part of the
`main` package. The `main` package on line 1 must contain the `main`
function on line 5.

The `main` function on line 5 is where the program begins
execution - not line 1. Program execution then proceeds in sequence from
this point onwards i.e. down the screen as you look at it. There must be
exactly one `main` function in any program. There must also be exactly
one `main` package in any program. The `package main` line must also be
the first line in the source code file. No program code can appear before
this line.

The next funny looking line is line 3.

{{< hilight lang="go" style="edit-gedit" lineNumbers="n" >}}
import "fmt"
{{< /hilight >}}

This  is a package import line. Before Go can use a package, it must
first import it. Packages contain lots of useful stuff written by
other programmers that you can use. This useful stuff is called
__functions__.

The name of the package that is to be imported must be places inside
inverted. In this case the program is importing he `fmt` package, short
for "Format", which contains the functions such as `Println` that prints
text to the terminal window.

Don't panic if you don't understand this yet. You will see these lines in
almost every Go program you write.
