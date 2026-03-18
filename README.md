# AOC_AMS

Every Advent of Code problem solved using TI-BASIC on an overclocked TI-89 Titanium graphing calculator. All TI-BASIC code was written on a physical TI-89 Titanium. Each solution is guaranteed to use <145 KBytes of RAM during execution.

**This is WIP; latest puzzle solved is `2015 Day 1 Part 2`** 

Expected input format and execution times for each solution are included in markdown files accompanying them. (Note that all these solutions were run on an overclocked machine running at roughly twice the stock clock speed. See [my post](https://www.reddit.com/r/overclocking/comments/1k1wp13/i_overclocked_my_ti89_titanium_from_123_mhz_to/) for more info.)

All materials in this repository are under the [MIT License](./LICENSE).

## Terminology

* "AMS" = the operating system that the calculator runs (very embedded-esque, non-multitasking). Very technically different from the OS that TI-84 Plus types of calculators run.
* "TI-BASIC" = the interpreted, non-JIT scripting language the calculator is designed to be programmed with
* "m68k" = The [Motorola 68000 CPU](https://en.wikipedia.org/wiki/Motorola_68000), one of the most influential CPUs of all time, a low-power embedded version of which is used in the TI-89 Titanium 

## FAQ

###### (No one has ever asked me questions about this but I might as well put them here anyway. I'm a sicko, I know.)

### Why BASIC on a TI graphing calculator?

I don't know, it just felt like it'd be a ton of fun. Something about coding in an interpreted language that's old enough to drink and drive running on a [half-century-old processor architecture](https://en.wikipedia.org/wiki/Motorola_68000#:~:text=Introduced-,1979%3B%2046%20years%20ago,-Design) with roughly 145 KB of available RAM is exciting to me. And yes, I actually code using the buttons on the calculator itself. (You get used to the layout after a while, plus the UI is far more computery than you may expect.)

### What's the execution speed like?

Eric Wastl confidently claims on the Advent of Code website's 'About' page that ["every problem has a solution that completes in at most 15 seconds on ten-year-old hardware."](https://adventofcode.com/2024/about#:~:text=every%20problem%20has%20a%20solution%20that%20completes%20in%20at%20most%2015%20seconds%20on%20ten-year-old%20hardware.) Clearly he has not witnessed the horrors of BASIC execution speed on TI calculators. *Besides, my machine's design is 20 years old, not 10.*

All execution timings are included in a plaintext file called `details.txt` in each solution's respective folder. These were measured with a program called `hrglass` (hourglass) in the `_deps` directory, that returns the number of seconds it takes for a program call wrapped in a string to return. (With the timescales we're dealing with on this dinosaur platform, there is really no need for sub-second precision.)

Most of the solutions take more time to run than they do to code, and that's *after* I overclocked my calc to double its original speed. I know if I made these on a TI-Nspire (which uses a semi-modern ARM processor many times faster than an embedded m68k) then my solutions would run much faster, but who needs speed when you've got novelty?

### So what if it's running on an m68k with 145 KB RAM? You're coding in an interpreted language.

That's correct, and I mentioned it in the first FAQ's answer for a reason. I don't want to make myself look like some sort of assembly wizard, which I'm not. There's just a certain 'feel' to TI-BASIC on AMS, and although you don't have 100% control over memory contents, it is fun to figure out how to elegantly mold my solution to the problem into the calc's highly unique set of programming features and datatypes. It is also [very well-documented](https://debrouxl.github.io/gcc4ti/estack.html#top_estack) and quite predictable because it's so relatively simple, so it's not like I'm unknowingly using gobs of memory either.

I suppose that I can also show that I know problem-solving so well that I can finish the entirety of Advent of Code with a language that the most powerful LLM in the world doesn't know - there simply isn't enough training data, as not many people have converted their TI-BASIC to plaintext and posted it on the Internet.

### Boo, you're just producing alkaline waste!

Before you complain that I'm harming the environment by coding on a calculator that only runs on AAA batteries, please note that I've been using only rechargeable NiMH cells to do all these solutions. Less waste, but more wasting my time working on this repo!
