_Fill in each this file with your responses, placing each response after its
corresponding question._

---

**Question**

Pick three quotes from the readings about language design. Good candidates 
are:

   + Something you agreed with / resonates with your own experience
   + Something you disagree with
   + Something that is interesting, a new idea or perspective you'd like to remember
   + Something you didn't understand

For each quote, describe what it was about the quote that led you pick it.

**Response**


1. "Many brilliant and talented people have contributed to R over the years, many
of whom are renowned computer scientists for whom I have tremendous respect!
But a computer scientist is not the same as a software engineer." [Smith, 2016]

We picked this quote because while most of what we have been reading has been 
from professors and researchers who study the design and implementation of 
languages, we rarely get a voice from an "outsider" in this respect - someone 
who just wants to use a language for a purpose and not to analyze its history 
and design decisions. We think the goal of a well-designed and "good" DSL is to 
be a tool that accomplishes the domain-specific goals easily or intuitively. 
Smith does not think R is not well-designed, and traces the cause to the lack 
of software engineers contributing to R.

The author specifically makes the distinction between computer scientist and 
software engineers, which brings up differences between academia and industry. 
However, many languages developed for and used by academia are very planned 
and are implemented very specifically, i.e. Prolog and Lisp. Languages 
that are considered better designed than R also have a lot of contributions 
from computer scientists who are not software engineers, so it doesn't seem 
like that is the reason why R is badly designed.

Doing some research, it seems that R was derived from S, with some language 
components inspired by Scheme. It was developed by two people initially, and 
now its design is directed by the R-core of around twenty people. It is unclear 
how many of those people still actively contribute, and maybe that is the 
problem. Maybe because R is open-source, a kind of a project built as a bazaar, 
it incorporated too many different designs and features that, when looked at 
together by a newcomer, seems like a series of hacks and a mishmash of things. 

2. “The key point is that in the bazaar style of building a program or designing a language or what you will, the plan can change in real time to meet the needs of those who work on it and use it. This tends to make users stay with it as time goes by; they will take joy in working hard and helping out if they know that their wants and needs have some weight and their hard work can change the plan for the better.”


We chose this quote because we feel that Steele’s point seems to be a very true pattern across many of the popular languages today. A typical example of this would be Javascript, which was created around 20 years ago within the span of 10 days. It was meant as a sort of “glue” language to build web apps, with the “components” being written in Java. Fast forward a decade and a half and so many useful open-source libraries have been created, some of which have widespread communities. Who could have predicted early on that we can eventually use JavaScript on the server-side? Meanwhile, languages that did not allow for this style of open-source, pivoting growth like Pascal and PL/I are now the stuff of history books. 

It is interesting, however, to consider Java as a counter-example. It was not until 2006 that Sun released most of its JVM as free and open-source. The development of Java as a programming language did not really follow Steele’s ‘bazaar-style’, yet was still widely used. This may have partly been because it was modeled on the syntax of C/C++, but intended to simplify certain things like memory management. In that sense, there were less risks involved in the creation of Java as opposed to earlier programming languages. 



3. “Programming languages are tools, designed by people for a specific purpose. What this study showed is that the design of this particular tool, Perl, is so ridiculously opaque that, from the perspective of a novice programmer, a string of characters bashed out by a monkey at a keyboard would literally make an equal amount of sense… "We have observed that novices learning to program at the university or younger levels can have signiﬁcant difﬁculty learning the syntax of general purpose programming languages, which may initially seem arbitrary," the authors [of the study wrote].”

We found this article, and in particular, this quote rather hard to believe so we decided to further investigate the validity of this claim in the additional optional reading.  It was rather surprising to see that the subjects performed better on coding tests using Randomo than Perl after being shown a code sample in their respective language (with an accompanying explanation of what the code does). Just looking at the code samples, it seems much easier to intuit how the Perl code functioned compared to Randomo. This may be because as programmers, certain syntax – like for loops - that look familiar to us are foreign to the test subjects who had no prior programming experience. Even though we had basically no exposure to Perl (Julien had seen a little bit), we were able to figure out how the Perl code worked. 

Our main issue with Randomo is that it is not the “string of characters bashed out by a monkey” Pavlos rather dramatically portrays it to be. To quote the study: “Randomo: A programming language based largely on the syntactical structure of Quorum. With the exception of braces, the lexical rule for variable names, and a few operators (e.g., addition, subtraction, multiplication, division), many of the keywords and symbols were chosen randomly from the ASCII table.”

This means that it by and large works syntactically as Quorum does – the language designed following “empirical studies on intuitiveness” -  with the biggest difference being the random keywords and symbols. To a complete beginner, constructs like for loops and symbols like “==” and “++” would have no inherent meaning and it’s almost understandable that random symbols such as those used in Randomo would at least be as easy to understand. 

As a whole, we thought the main point of the article written by Pavlos was misleading. 

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

A well-designed language is made up of many things. A few symptoms are 
intuitiveness, ability for growth, well-defined semantics and langauge building 
blocks. There are a few more symptoms when talking about a well-designed 
language for industry-use and some other symptoms if we are talking about a DSL.

We defined intuitiveness to mean something that is relatively easy to read and 
write. By "easy to read and write" we don't mean easy to read and write for 
someone who's never programmed before (which seems to be what Pavlus is 
advocating in his article [Pavlus, 2012]). Rather, for someone's who's seen or 
used a few languages, maybe taken CS5 and CS60, can they read and possibly 
start writing code in this language quickly?

A language that is well-designed does not always have to be extensible and 
allow for growth, but allowing the language to be modified by people other than 
the creators allows for a bigger community which makes the language more 
supported. Steele talks about this extensively in his article, "Growing a 
Language" [Steele, 1998]. A language that does not get a following or have a 
community will soon die. Though one cannot definitely say a dead language or 
one that is unused / used by very people means it is a badly designed language, 
we think there is definitely a correlation. Steele touches on this by talking 
about Java and how he and others that work on Java do not define the way it is 
going, but rather a "way of doing things". 

Another symptom of a well-defined language is that it has well-defined 
semantics / language building blocks. This contributes to the elements above, 
specifically, the easiness to read and write. More importantly, well-defined 
semantics and building blocks makes the language predictable. As Jean Yang says, 
a good programming language should have well-defined semantics that "make it 
easy to reason about what your program will do" [Yang, 2012].

For languages use in industry, there are a few more elements that contribute to 
a well-designed language. Nystrom, in his article about what makes a well-
designed languages, talks about how a well-designed languages should be 
scalable for large systems and teams over time [Nystrom, 2011]. These are some 
things we have not talked about in class, but are very important when choosing 
languages in industry. For example, Go is seeing a rapid rise in popularity in 
industry because of the easiness of doing concurrency in Go. 

For DSLs, there are even more considerations. "Well-known GPL design criteria 
such as readability, simplicity, orthogonality,the design principles listed by 
Brooks[1996], and Tennent’s design principles [1977] retain some validity for 
DSLs. However, the DSL designer has to keep in mind both the special character 
of DSLs as well as the fact that users need not be programmers" [Mernik et al., 2005]. 
Mernik et al. go on to talk more about the specifics of good DSL design, but this 
quote is important as it talks about how when designing a DSL, one should be 
aware of the language's audience, and the nature of the domain the language is 
for. 

There are also many things that make a language badly-designed. Some obvious 
symptoms are bad naming conventions and contradicting popular conventions.
If a language's key words contradict those used by popular language, for 
example, if "break" in some language means exposing elements from an array 
instead of interrupting a loop procedure, then it can be seen as bad language 
design. 

If a langauge has ambiguities and uncertainties, then it is also badly 
designed. Though JavaScript is very widely used, it is some ambiguities that 
make it a badly-designed language. For example, the "this" keyword is used 
differently in different but very similar contexts. This can easily confuse and 
makes debug harder to do.

[Yang, 2012] https://www.quora.com/What-makes-a-good-programming-language/answer/Jean-Yang?srid=z8gA
[Nystrom, 2011] http://www.monomorphic.org/wordpress/what-makes-a-good-programming-language/ 

---

**Question**

How do the themes of _Growing a Language_ relate to the "sound lab" we did this week?

**Response**

In the Sound lab, we brainstormed ways to modify existing files to make it easier to chain together function calls, for instance, to change the volume and reverse the sound file. Common ideas were to rename function names for clarity, and to eliminate the redundant arguments. We grappled with the benefits and drawbacks of a functional style method-chaining versus the imperative method-chaining. 

In hindsight, this activity was reminiscent of Steele’s “bazaar” style of development. We were given the results of a CS5 problem set to start with; it seemed like a group of programmers had created a DSL to interact with sounds and we were essentially iterating on top to make it more intuitive to use. We had full control of how we wanted it to develop and could enjoy the fruits of our hard work if we had decided to follow through with some of our ideas.  

On the other hand, because we were to first explore on our own we all had different ideas of how to approach the problem. In this sense, we got a taste of what it would be like to be the solo designer implementing our own “master plan”. Once we came back to a group discussion, it was interesting to see that many of us had similar ideas, but even more intriguing to see where we diverged. It was quite clear from this exercise that the bazaar approach is in general superior to the cathedral approach. 


---
 
**Question**


In what way is an API a language? 

**Response**

An API is similar to a language stripped of its fluency. It consists of 
methods, but with no real way to chain the methods together. Instead, this, 
and other flow control statements need to be done in a host language. However,
a well-designed API should have many features of a well-designed language. 

In Bloch's talk on APIs, many of the guidelines about designing a good API is 
also good advice for creating a well-designed language. For example, Bloch says 
a well-designed API should have good names and strive for "intelligibility, 
consistency, and symmetry" [Bloch, 2006]. This is similar to our points in the 
previous questions regarding how a language should be intuitive and not be 
ambiguous. 

Many things around implementation of APIs are also similar to 
languages, as languages and APIs should, according to Block, avoid showing 
the user its internal implementations, and "Consider the performance 
consequences of" the design decisions. 


---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

It was very interesting to see the process of re-designing the greyscale function and the community feedback.  One of the most things we took away from the post was how different people’s opinions were. Maybe it’s a result of our experiences with other software or simply personal preferences, but what may seem natural to one person is not to another. This is illustrated by the results of the survey: https://docs.google.com/forms/d/e/1FAIpQLScOvDU75W-UNPqDmVScprsO0YT6R_NJr1ZUjllrdNSf3pQPAA/viewanalytics?usp=form_confirm

Both of us agreed with the majority result of the survey as the best option (none of the other options were that intuitive), although we both thought that even this was not a perfect solution because it is not that obvious and may be difficult to debug just from looking at ‘rgb’ values. Even an anonymous survey like this has inherent bias because most of the responses are from people with front-end dev or CSS experience so it is hard to tell which option novices find the most intuitive. 

It was also quite interesting to see community feedback and the debate in the comments section. For instance, someone suggested using grayscale() which is used widely by designers, but it turns out that function name is already used as a filter. Perhaps the most important takeaway was that it takes several iterations to get something right, so API or DSL designers should not only be open to change but actively looking for it. 


---

**Question**

The Yang and Rabkin article talks mainly about general-purpose languages. In 
what ways do the themes apply to the study and creation of DSLs?

**Response**

The language stereotypes explored in the Yang and Rabkin article are very much applicable to the use of DSL’s. People who use DSL’s are susceptible to this same “language-based snobbery”. Consider the example of jQuery. In one of Julien’s previous internships, jQuery was scoffed at – although there were performance-related improvements to its eventual removal. Even though it is widely used and no doubt simplifies interactions with HTML, some programmers may think of it as a crutch, and a sign of weakness as it removes the need to understand the DOM on a deeper level. 

Just like general-purpose languages, domain-specific languages are judged based on their perceived users rather the language itself. This prejudice is harmful to DSL’s in an additional way. Users may shy away from using a DSL because of the public image of its users. 

On the other hand, in Justin’s internship, the use of proprietary DSL’s was basically mandatory. The nature and size of the codebase meant that the company had to create its own DSL’s, and had teams of people to provide support. 



---

**Question**

The Pavlus article mentions the researchers' comments that people preferred
"natural-language replacements for some of the more abstruse syntax". In other 
words, people found it easier to work with code that looks more like a human language (e.g.,
English). Consider the following quote by William R. Cook, one of the creators
of AppleScript:


> The experiment in designing a language that resembled natural languages (English
> and Japanese) was not successful. It was assumed that scripts should be
> presented in “natural language” so that average people could read and write
> them. … In the end the syntactic variations and flexibility did more to confuse
> programmers than to help them out. It is not clear whether it is easier for
> novice users to work with a scripting language that resembles natural language,
> with all its special cases and idiosyncrasies. The main problem is that
> AppleScript only appears to be a natural language: in fact, it is an artificial
> language, like any other programming language. … even small changes to the
> script may introduce subtle syntactic errors that baffle users. It is easy to
> read AppleScript, but quite hard to write it.
[[Cook 2007, page 1-20]](https://dl.acm.org/citation.cfm?doid=1238844.1238845)

Are these two experiences of natural languages at odds with one another? Would
you choose to include natural language in the design of a DSL? If so, how might
you do so? If not, why not?

**Response**

These experiences of natural languages are not at odds with one another. 
Pavlus only mentioned "natural-language replacements for some of the more 
abstruse syntax". Perhaps what happened with AppleScript was too much similarity 
with natural languages. 

The study Pavlus talked about referred to the language Quorum, which seems like 
a very similar language to Python. Python is also a language that is seen as 
very beginner friendly. Many of its syntax is, like Quorum, very "natural" to 
someone who has not programmed before, for example, "if number in numbers." 
However, Python would never be mistaken for any natural language in even a 
brief inspection - neither would Quorum. Once a language is too much like 
natural languages, the user might use their instincts in the natural languages 
to solve the bugs, but that would probably not work (as Cook pointed out).

We would use natural languages in the naming of keywords. However, neither of 
us would use natural language as a model for our syntax. Too similar to, say, 
English, would cause problems similar to what we speculate happened to 
AppleScript - people would be in a natural language mindset and use their 
instincts in that natural language to write or debug their programs, which 
often does not work.

We would instead use more concrete and programming language-like syntax, as we 
can make sure that is more concrete, and makes sure the user is in the mindset 
of writing the DSL, and not in some state where they are mixing the DSL with 
English or anything else.

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

We completed all the readings independently, then came back to discuss our thoughts. After collectively writing an outline, we wrote up each answer individually. Then, we reviewed each others' responses, modifying them accordingly 


---
