Download Link: https://assignmentchef.com/product/solved-csf211-assignment4
<br>
<h1>Changelog</h1>

<ul>

 <li>Question B – testcase 2 has been corrected. The earlier answer was incorrect.</li>

 <li>Question C – clarification – all words shall consist of lowercase English alphabets only.</li>

 <li>Question D – constraints for <em>N </em></li>

 <li>Question F – Input format for corrected</li>

 <li>Question I – pseudo code corrected from <em>r </em>= <em>n </em>− 1 to <em>r </em>= <em>n</em></li>

</ul>

<h1>A: Sky of a Million Stars</h1>

A cave discovered on Mars appears to have a bunch of inscriptions in the wall, presumably made by an alien race. Linguists and anthropologists who are studying the images beamed back to Earth realised that they could piece together some of the information if they knew the order of that foreign alphabet. The alien race, surprisingly, uses a <strong>subset </strong>of the English alphabet [A-Z], but with a different alphabets order. Experts studying the inscriptions could discover <em>N </em>rules about the alien alphabetical order. Each rule is represented as <em>c</em><sub>1 </sub><em>c</em><sub>2</sub>, meaning letter <em>c</em><sub>1 </sub>comes before <em>c</em><sub>2 </sub>in the alien alphabet. Note that all alphabets that are a part of the alien alphabet <strong>will definitely </strong>appear atleast once in the rules. Print <strong>one </strong>valid order of the alien alphabet. If there are multiple alien alphabet orders possible, print any one. If the alien language is self-contradictory, print “ALIENS BE CRAZY” and exit.

<h2>Input</h2>

The first line contains an integer). The next <em>N </em>lines contain two characters each

(space-separated), representing one rule. It is guaranteed that all characters in rules are capital letters A-Z.

<table>

 <tbody>

  <tr>

   <td width="122"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<h2>Output</h2>

The order of the alien alphabet in one line, with no spaces. If no order is possible, print the string “ALIENS BE CRAZY”.

input

8

input

R E

3

<ul>

 <li>SX B</li>

 <li>AC X</li>

</ul>

E A C A

L M

<ul>

 <li>R</li>

</ul>

output

<ul>

 <li>X</li>

</ul>

CAXB X A

explanation

output

Other possible answers are CXAB,

ALIENS BE CRAZY

CXBA

explanation

No valid outputs possible.

<h1>B: The Three Laws</h1>

<em>A robot may not injure a human being, or, through inaction, allow a human being to come to harm.</em>

In a bid to garner publicity for their new line of security and police robots, U.S. Robots is organising a RoboWars event that will be televised on international TV. The tournament has <em>N </em>robots participating, each with strength <em>R<sub>i</sub></em>. When a robot with strength <em>R<sub>i </sub></em>fights with a robot of strength <em>R<sub>j</sub></em>, the robot with higher strength wins, and destroys the weaker robot. The weaker robot is completely destroyed and eliminated from the tournament. The stronger robot (say, <em>R<sub>i</sub></em>) survives, but it’s strength changes to <em>R<sub>i</sub></em>(<em>new</em>) = <em>abs</em>(<em>R<sub>i </sub></em>− <em>α</em>(<em>R<sub>i </sub></em>− <em>R<sub>j</sub></em>)), where 0 ≤ <em>α </em>≤ 10. If two robots are equally matched, they both die in each others hand. The tournament consists of a number of rounds, which continue till only one (or none) robots are left standing. The robots are initially placed in a straight line, and in the first round, the first robot fights the second, the third robot fights the fourth and so on. If a robot is leftover at the end of the line, and can’t be paired it doesn’t take part in the round, and recharges while everyone else fights, allowing it to increase its strength by <em>β </em>in that round. Once the round is complete, dead robots are removed and the next round commences. Determine the position and final strength of the winner.

<h2>Input</h2>

The first line contains three space separated integers – <em>N </em>(0 ≤ <em>N </em>≤ 10<sup>5</sup>), <em>α </em>(0 ≤ <em>α </em>≤ 10) and <em>β </em>(500 ≤ <em>β </em>≤ 10<sup>3</sup>). The next line contains <em>N </em>space separated integers numbers, denoting the strengths of each of the robots in line. (0 ≤ <em>R<sub>i </sub></em>≤ 10<sup>4 </sup>∀<em>i</em>).

<h2>Output</h2>

Print two space separated numbers <em>i </em>and <em>R<sub>f</sub></em>. <em>i </em>is the position the final surviving robot (winner of the tournament) was standing in at the start of the tournament (the initial line is 1-indexed). <em>R<sub>f </sub></em>is the strength of the winner after the final round. If no robots are left standing print −1 − 1.




input

5 5 30 70 75 80 80 20 output

-1 -1

explanation

<table>

 <tbody>

  <tr>

   <td width="5"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

After the first round, the robot strengths are: {50, 50} – which leads to both of them dying in the final round. No robot left standing..

input

7 8 40 70 60 50 120 100 50 40

<table width="236">

 <tbody>

  <tr>

   <td width="112">After round 1:</td>

   <td width="125">{10, 440, 300, 80}</td>

  </tr>

  <tr>

   <td width="112">After round 2:</td>

   <td width="125">{3000, 1460}</td>

  </tr>

  <tr>

   <td width="112">After round 3:</td>

   <td width="125">{9320}</td>

  </tr>

 </tbody>

</table>

output 4 9320

explanation




<h1>C: Talking to Myself</h1>

Mike likes playing a word game with himself, where he tries to transform a word, <em>S </em>(length <em>M</em>), to a different word <em>E </em>(length <em>M</em>). He begins by changing (replacing) one letter of the <em>S</em>, to form an intermediate word <em>W</em><sub>1</sub>. He then changes another letter in <em>W</em><sub>1 </sub>to form <em>W</em><sub>2</sub>. He does this to form a sequence of words <em>S,W</em><sub>1</sub><em>,W</em><sub>2 </sub><em>…W<sub>L</sub>,E</em>. The end word is special, since it must satisfy the property <em>E</em>[<em>i</em>] 6= <em>S</em>[<em>i</em>], ∀<em>i </em>such that 0 ≤ <em>i </em>≤ <em>M </em>− 1. Additionally, he cannot arbitrarily replace any letter with another letter – all intermediate words (<em>W<sub>i</sub></em>) and the end word (<em>E</em>) must be real words, which means they must be in a dictionary <em>D </em>(containing <em>N </em>words). Determine if such an <em>E </em>exists, and if it does find the <em>minimum </em>number of intermediate words required to get to an end word <em>E </em>from the start word <em>S</em>. If it is impossible to do so, print −1. If there are multiple possible words E, choose the one that has a minimum number of intermediate steps. <em>Additional thinking: if you had to implement this for the entire English dictionary, would your approach work?</em>

<h2>Input</h2>

The first line of the input contains integer <em>N </em>such that 1 ≤ <em>N </em>≤ 1000. The second line of input contains the word <em>S</em>. The next <em>N </em>lines contain one word each (<em>D<sub>i</sub></em>) such that 1 ≤ <em>len</em>(<em>D<sub>i</sub></em>) ≤ 12 representing all words in the dictionary. All words consist of lowercase English letters only.

<h2>Output</h2>

Output a single integer, denoting the <strong>minimum </strong>number of intermediate words you’d need to generate before reaching an end word.

input 1

input 2

9

9

app rome

xi tome

ben some

ape hell

apo hall

xu peep

ave xhud

bpo yyee

beo yuii

ove

iyll

output 1

output 2

2

-1

explanation 1 app -&gt; ape -&gt; ave -&gt; ove. ove is an end word, by definition, and we need two intermediate words to get here. app -&gt; apo -&gt; bpo -&gt; beo -&gt; ben is also a valid path, with end word “ben”, but this has 3 words.

<h1>D: Wikipedia</h1>

<em>TIME Person of the Year, 2006</em>

Rohan began reading a Wikipedia article <em>S </em>initially. In each Wikipedia article, there are links to other Wikipedia articles. Being the curious lad he is, one of the links <strong>might </strong>interest him, causing him to click on it and read the linked article. However, he doesn’t pick what article to choose out of the links at random – for each link in an article, there is a certain probability (<em>p<sub>ij</sub></em>) that Rohan will click it. There is also a probability (<em>q<sub>i</sub></em>) that he will not click on any link at all, and just close the browser after reading the current article. This probability <em>q<sub>j </sub></em>for a certain article, can be calculated as <em>q<sub>j </sub></em>= 1−<sup>P</sup><em><sub>i </sub>p<sub>ij</sub></em>, where <em>p<sub>ij </sub></em>is summed over all outgoing links on that article. Some articles might not have any outgoing links, meaning he will shut down his browser after reading that last article. Given a set of links (<em>E</em>) and probabilities associated with clicking each link, calculate, for each article, the probability that it is the last article he reads. It is guaranteed that articles (<em>W<sub>i</sub></em>) and edges (<em>E</em>) form a tree rooted at <em>S</em>. Rank all articles from highest to lowest probabilities of it being the last article read.

<h2>Input</h2>

The first line has integers <em>N </em>(1 ≤ <em>N </em>≤ 10<sup>5</sup>), <em>E</em>, and <em>S</em>. The next <em>E </em>lines contain three space separated numbers – (<em>W<sub>i</sub>,W<sub>j</sub>,p<sub>ij</sub></em>) – meaning that article <em>W<sub>i </sub></em>has a link to <em>W<sub>j</sub></em>, and there is a <em>p<sub>ij </sub></em>probability that this link will be clicked.

<h2>Output</h2>

Print <em>N </em>space separated numbers, the articles ranked in descending order of probabilities. If two articles have the same probability, order them in increasing order of article number.

explanation

Probabilities for ending on articles {0<em>..</em>9} are {0.3, 0.01, 0.2, 0, 0.16, 0.06, 0.04, 0.03, 0.06, 0.14} respectively. Article 0, which has the highest probability (0.3), is printed first. Articles 2, 4, 9 have the next three highest possibilities (0.2, 0.16, and 0.14). The next highest probability of 0.06 is shared by articles 5 and 8 – 5 must be printed before 8, as 5 <em>&lt; </em>8.

<h1>E: Connecting Nails</h1>

On a wooden plank, you have <em>M </em>nails driven into the wood at points <em>S </em>= {(<em>x</em><sub>1</sub><em>,y</em><sub>1</sub>)<em>…</em>(<em>x<sub>M</sub>,y<sub>M</sub></em>))}, with each nail being one point. Nails are connected in this order: sweep a reference line from the X axis upwards (order of quadrants: Q1, Q2, Q3, Q4), completing a full turn while joining every subsequent point. Let <em>S</em><sub>0</sub>, <em>S</em><sub>1 </sub>be the first two vertices encountered while sweeping the line, and let <em>d</em><sub>0 </sub>be the Manhattan Distance between them. Calculate the sum of all pairwise Manhattan distances (<sup>P</sup><em><sub>i </sub>d<sub>i</sub></em>) between all such pairs of points encountered as the reference line sweeps all four quadrants It is guaranteed that, for any two distinct points <em>I</em>(<em>x<sub>i</sub>,y<sub>i</sub></em>), <em>J</em>(<em>x<sub>j</sub>,y<sub>j</sub></em>), I, J and the origin <em>O</em>(0<em>,</em>0) are never collinear if <em>I </em>and <em>J </em>are in the same quadrant.

<h2>Input</h2>

The first line contains the number <em>M</em>. The next <em>M </em>(3 ≤ <em>M </em>≤ 10<sup>5</sup>) lines contain two space separated integers representing <em>x<sub>i</sub>,y<sub>i </sub></em>(−1<em>.</em>5 ∗ 10<sup>5 </sup>≤ <em>x<sub>i</sub>,y<sub>i </sub></em>≤ 1<em>.</em>5 ∗ 10<sup>5</sup>).

<h2>Output</h2>

Print one integer, <em>L</em>, the sum of all pairwise Manhattan distances.




figure

The answer to the above problem is the sum of all Manhattan distances of the points connected by red line segments, i.e. <sup>P</sup><em><sub>i </sub>d<sub>i</sub></em>. Orange arrow indicates the beginning point, and the direction to rotate our reference line.

input 3

4120 0

-1000 9800 -3210 -6467

output 47194

input 4

-1 6

1 1

4 -3

-1 -2

output 28

explanation Order of points: (1<em>,</em>1), (−1<em>,</em>6),

(−1<em>,</em>−2), (4<em>,</em>−3), (1<em>,</em>1)




<h1>F: Polifia</h1>

Tim is a guitar player and wants to hold a concert. The venue can be represented by a cartesian co-ordinate plane. Tim has <em>N </em>amplifiers where the <em>i<sup>th </sup></em>amplifier has a power output of <em>a<sub>i </sub></em>watts and is located at the position (<em>x<sub>i</sub></em>, <em>y<sub>i</sub></em>). Each of these <em>N </em>amplifiers has already been placed in the venue by the sound engineer and cannot be moved. There is something very peculiar about this particular venue: The people in the crowd can only stand along <em>some line parallel to y </em>= <em>x</em>. Note that this line is chosen by Tim and can be placed anywhere in the co-ordinate plane. Tim wants the audience to get an equal volume of sound from both sides so he wants to place the line such that the <em>sum of powers of amplifiers on both sides of the line is equal</em>. Help Tim find if placing such a line is possible. More formally, you must find if it is possible to choose a line <em>y </em>= <em>x </em>+ <em>c </em>where <em>c </em>is a variable such that sum of powers of amplifiers on both sides of the line is equal.

<h2>Input</h2>

The first line of input contains one integer <em>T</em>, the number of testcases. For each testcase, there will be <em>N </em>+ 2 lines of input as described below. The first line of each testcase consists of <em>N </em>(1 ≤ <em>N </em>≤ 10<sup>5</sup>), the number of amplifiers. The next <em>N </em>lines contain three integers each: <em>x<sub>i</sub></em>, <em>y<sub>i</sub></em>, and <em>a<sub>i </sub></em>the co-ordinates of the <em>i<sup>th </sup></em>amplifier (−10<sup>9 </sup>≤ <em>x<sub>i</sub>,y<sub>i </sub></em>≤ 10<sup>9</sup>) and the power of the <em>i<sup>th </sup></em>amplifier (−10<sup>9 </sup>≤ <em>a<sub>i </sub></em>≤ 10<sup>9</sup>)

<h2>Output</h2>

Print <em>T </em>lines, with each line containing either YES or NO in all capitals. (please print in all capitals to avoid problems with Mooshak)

input 1

3

<ul>

 <li>1 3</li>

 <li>1 1</li>

</ul>

1 -1 4

output YES

explanation

We have one testcase. Any line of the form <em>y </em>= <em>x </em>+ <em>c </em>∀− 2 <em>&lt; c &lt; </em>2 would divide the amplifiers such that both sides have a total power of 4 watts

<h1>G: Tuul</h1>

Danny Carey has <em>N </em>drum pads lined up in a row, where the <em>i<sup>th </sup></em>drum pad has a frequency <em>a<sub>i</sub></em>. For the next song Danny needs all the drums pads to be arranged in a non-decreasing order of frequencies. In one swap, Danny can swap the positions of two adjacent drum pads. He needs to quickly tell his drum mechanic the minimum number of such swaps required to arrange the drum pads in a non-decreasing order of frequencies. Despite being a natural at polyrhythms, he was too slow at this task so he asked you for help.

Hint: Try and think of a divide and conquer strategy

<h2>Input</h2>

The first line of input contains a single integer <em>N </em>(1 ≤ <em>N </em>≤ 10<sup>5</sup>), the number of drum pads. The second line contains <em>N </em>integers, where <em>a<sub>i </sub></em>represents the frequency of the <em>i<sup>th </sup></em>drum pad (−10<sup>9 </sup>≤ <em>a<sub>i </sub></em>≤ 10<sup>9</sup>).

<h2>Output</h2>

output a single integer, the minimum number of swaps required to arrange the drums as described above.

input 5

1 20 6 4 5

output 5

explanation

first swap 20 with 6, then 20 with 4, then 20 with 5. Then swap 6 with 4 and then

6 with 5. With a total of 5 swaps, we get the arrangement 1 4 5 6 20

<h1>H: Meshuguhh</h1>

Fredrik Thordendal wants to make an ironic song using only the major scale to confuse his fans. The major scale consists of 7 notes, represented by the upper case letters A to G (inclusive). He writes out a riff for this (in drop F tuning obviously) using these notes. Here, a riff is a sequence of notes where each note is a capital letter from the set of letters A to G (inclusive). The drummer Thomas noticed that the riff was way too long so he asked Frederik to choose the <em>smallest possible contiguous subsegment </em>from the riff that contains <em>all </em>the types of notes present in the riff, and use that for the song. Can you help Frederik find the length of such a subsegment? More formally, your task is to find the smallest subsegment such that the set of distinct notes in the subsegment should be equal to the set of distinct notes in the entire riff.

<h2>Input</h2>

The first line contains a single integer <em>N</em>, the number of notes in the entire riff (1 ≤ <em>N </em>≤ 10<sup>5</sup>). The second line contains a string of characters representing the riff itself. It is guaranteed that the string only consists of upper case english letters from A to G (inclusive).

<h2>Output</h2>

print a single integer, the length of the smallest possible contiguous subsegment that contains all the types of notes contained in the original riff

input 9 ABBGDCACD

output 5

explanation

We can take the subsegment from index 3 to index 7 (inclusive). This subsegment includes the notes B,G,D,C,A which contains all the notes present in the entire riff

<h1>I: Melattica</h1>

Lars Ulrich isn’t a very good drummer so he decided to use a Machine Learning model to write drum parts for him. But now the rest of the band likes the machine learning model better and decides to fire Lars. Now he has to use his machine learning skills in other ways. He develops a model that can check if a permutation is in increasing order or not but he’s not sure if the model actually works. To check this, he decided to perform a test: he takes a number <em>x </em>and expects it to be at position <em>pos </em>if the permutation is sorted. He then performs a binary search on the permutation and if the number <em>x </em>is at position <em>pos </em>according to the binary search, then he says that the permutation is increasing. (Recall that a permutation of size <em>N </em>is an array such that every number from 1 to <em>N </em>occurs exactly once). The C code for the binary search he performs is given below

<strong>int </strong>l =0, r=n; <strong>while</strong>( l<em>&lt;</em>r ) { mid = ( l+r )/2; <strong>if </strong>( arr [ mid]<em>&lt;</em>=x) l = mid+1;

<strong>else </strong>r = mid ;

}

l<em>&gt;</em>0 &amp;&amp; a [ l −1]==x? printf (”Yes”)                      :        printf (”No” );

<table>

 <tbody>

  <tr>

   <td width="122"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

But what Lars doesn’t know is that the permutation need not be necessarily sorted to find the number <em>x </em>at position <em>pos</em>. Can you find how many such permutations exist such that the binary search algorithm finds <em>x </em>at the position <em>pos</em>? Since the number can be large, print the answer modulo 10<sup>9 </sup>+ 7

source for those interested: <a href="https://www.youtube.com/watch?v=iTXU9Z0NYoU&amp;feature=emb_logo">NSynth</a><a href="https://www.youtube.com/watch?v=iTXU9Z0NYoU&amp;feature=emb_logo">,</a> <a href="https://www.youtube.com/watch?v=UWxfnNXlVy8">using neural networks to create melodies</a>

<strong>Input</strong>

The first line contains three numbers, <em>N,x, </em>and <em>pos </em>(1 ≤ <em>x </em>≤ <em>N </em>≤ 1000, 0 ≤ <em>pos </em>≤ <em>N </em>− 1).

<h2>Output</h2>

Print a single integer, the number of possible permutations modulo 10<sup>9 </sup>+ 7

input

4 1 2

output 6

explanation the binary search works on (2,3,1,4) , (2,4,1,3), (3,2,1,4), (3,4,1,2), (4,2,1,3), (4,3,1,2)

<h1>J. Zero Selects</h1>

You are giving the second round of inductions for the music club and the keyboardist plays a ”arpeggio” of <em>N </em>notes consecutively on his keyboard. You can tell from the sound that all the notes first increase to a certain point and then decrease till the end (Note that there can be 0 increasing or 0 decreasing notes). You are able to figure out the sequence of notes he plays and have stored that sequence in your memory where the <em>i<sup>th </sup></em>note played is <em>a<sub>i</sub></em>. The keyboardist then asks you <em>q </em>questions, where in the <em>i<sup>th </sup></em>question he asks if he played the note <em>t<sub>i </sub></em><strong>anywhere </strong>in the sequence. You have to correctly answer YES or NO for all queries or you’ll have to wait another semester to get into the club! To help you out with this refer to this link on <a href="https://www.geeksforgeeks.org/ternary-search/">ternary search</a>

<h2>Input</h2>

The first line contains 2 integers <em>N </em>and <em>q </em>(1 ≤ <em>N,q </em>≤ 10<sup>5</sup>), the number of notes played and the number of questions asked. The second line contains <em>N </em>integers, representing the notes played. It is guaranteed that the notes first increase and then decrease as described above. The next <em>q </em>lines contain one integer each: <em>t<sub>i </sub></em>where <em>t<sub>i </sub></em>represents the <em>i<sup>th </sup></em>question (0 ≤ <em>t<sub>i </sub></em>≤ 10<sup>9</sup>).

<h2>Output</h2>

output <em>q </em>lines, each containing a single word YES or NO in all capitals. (Please use all capitals to avoid problems with mooshak)

input

6 4

1 3 7 5 4 2

2

5

6 8

output YES

YES

NO

NO