# What Hath Woz Wrought

In the summer of 1979, I abandoned grad school to start working at Apple Computer as a systems programmer. I was already thoroughly obsessed with their main product, the Apple II, so it was a dream come true to become an Apple employee and meet the amazing people behind the company.

|||
| :----- | :-- |
| grad school | 研究生 |
thoroughly  | ADJ完全的，绝对的(用来强调程度)  Thorough is used to emphasize the great degree or extent of something.  |
| obsessed | ADJ-GRADED（对…）着迷的;（受…）困扰的；（为…）心神不宁的 If someone is obsessed with a person or thing, they keep thinking about them and find it difficult to think about anything else. |

I became even more excited when I found out about the first project that I was slated to work on: an inexpensive little graphical printer. Most printers were large, loud and expensive, printing by impacting an inky ribbon. Apple collaborated with a small, local start-up named Trendcom that had a different approach, relying on coated thermal paper that darkened when heat was applied. The “print-head” was a column of seven tiny thermal elements that got hot when enabled. It was almost silent as it glided across the page, printing up to 80 characters per line at 40 characters per second.

|||
| :----- | :-- |
|slated to | V-PASSIVE预定;计划;安排 If something is slated to happen, it is planned to happen at a particular time or on a particular occasion. |
| impacting | VERB(对…)产生影响 To impact on a situation, process, or person means to affect them. |
| ribbon | N-COUNT(打字机或打印机的)色带 A typewriter or printer ribbon is a long, narrow piece of cloth containing ink and is used in a typewriter or printer. |
| collaborated | V-RECIP合作，协作(尤指著书或做研究) When one person or group collaborates with another, they work together, especially on a book or on some research. |
| approach | N-COUNT方法;态度;手段 Your approach to a task, problem, or situation is the way you deal with it or think about it. |
| coated | COMB in ADJ(与 sugar, plastic 等物质名词连用，构成形容词）表示“覆盖…的”，“裹有…的”  -coated combines with names of substances such as 'sugar' and 'plastic' to form adjectives that describe something as being covered with a thin layer of that substance. |
| thermal | ADJ热的;由热引起的;温度变化引起的 Thermal means relating to or caused by heat or by changes in temperature. |
| darkened | ADJ(建筑物或房间)黑暗的，漆黑的 A darkened building or room has no lights on inside it. |
| column | N-COUNT柱状物 A column is something that has a tall narrow shape. |
| glided | VERB滑动；滑行；悄悄地走 If you glide somewhere, you move silently and in a smooth and effortless way. |

Trendcom controlled their printer with a relatively expensive digital board that included a microprocessor and memory chips. Apple planned to buy printer mechanisms from Trendcom bereft of their digital board, saving almost a third of the total cost of the printer. Instead, we planned to use software on the Apple II to do most of the controlling. My job was to write that software.

|||
| :----- | :-- |
| relatively | ADV相对而言;比较起来;某种程度上 Relatively means to a certain degree, especially when compared with other things of the same kind.|
|bereft|ADJ-GRADED失去…的；丧失…的 If a person or thing is bereft of something, they no longer have it.|
||Trendcom是另一家公司，上边写的collaborated意思是苹果在和trendcom合作|

I was pleased by the similarities between the printer project and Apple’s floppy drive, an awesome design that was peak Woz, his crowning glory. Woz had taken a standard Shugart floppy drive, and discarded most of its pricey controller board, using the Apple II to do the work instead, which saved cost while increasing capacity, flexibility and performance. We were going to do essentially the same thing with the Trendcom printer, only this time I got to be Woz, or at least the software side of him.

|||
| :----- | :-- |
|pleased|ADJ-GRADED高兴的；喜欢的；满意的 If you are pleased, you are happy about something or satisfied with something. |
|floppy drive|软盘驱动器,古老的技术|
|peak|N-COUNT顶点；顶峰 The peak of a process or an activity is the point at which it is at its strongest, most successful, or most fully developed.|
|crowning glory|crowning glory是一个习语，指的是某人或某物的最伟大或最引以为傲的成就、特质或部分。在这个句子中，作者用“crowning glory”来形容苹果的软盘驱动器设计，意思是这个设计是沃兹尼亚克的最伟大的成就。|
|Shugart floppy drive | Shugart是软盘驱动器的一种品牌。Shugart Technology公司是软盘驱动器的先驱之一，他们在20世纪70年代开发了8英寸和5.25英寸软盘驱动器，这些驱动器成为了早期个人计算机的主要外部存储设备。Shugart的软盘驱动器在当时非常流行，并为个人计算机的发展做出了重要贡献.|
|pricey|ADJ-GRADED价格高的；昂贵的 If you say that something is pricey, you mean that it is expensive.|
|essentially | ADV-GRADED根本上;本质上 You use essentially to emphasize a quality that someone or something has, and to say that it is their most important or basic quality.|
| got to be | 有机会成为或得以成为|

The only other engineer on the project was Victor Bull, who was the hardware designer and project leader. Vic, who was smart with a dry sense of humor and a soft spoken, laconic manner, sat down with me on my second day of work and introduced me to the details of my new project. The printer software that I was to write would live on a 2K byte ROM chip on the interface board that Vic was designing. It needed to provide an easy way for the user to print the contents of their graphics screen and also to print 80 columns per line of text, from both Basic and Pascal. It also needed to be finished within a couple of months, so we could ship it in time for Christmas 1979, now less than five months away.

|||
|:---|:---|
|laconic|ADJ-GRADED寡言的；言简意赅的 If you describe someone as laconic, you mean that they use very few words to say something, so that they seem casual or unfriendly.|
|manner|N-SING态度;举止 Someone's manner is the way in which they behave and talk when they are with other people, for example whether they are polite, confident, or bad-tempered.|
|dry sense of humor|"Dry sense of humor"通常指的是一种幽默风格，它以冷静、轻描淡写的方式表达幽默，通常不依赖于夸张或情绪化的表达。这样的人通常以幽默的方式说话，但不会带有太多的情绪或表情。|

It took about a week to write the low level routines that managed the position and temperature of the thermal elements and paper. We decided that sending a “control-Q” to the printer should print whatever was displayed on the Apple II’s 280 by 192 graphics screen. After some coding and debugging, it was thrilling to watch the embryonic prototype print a sharp, clear rendition of the current hi-res screen.

|||
|:---|:---|
|routines|N-COUNT例行程序 A routine is a computer program, or part of a program, that performs a specific function.|
|thrilling|ADJ-GRADED扣人心弦的;激动人心的;引人入胜的 Something that is thrilling is very exciting and enjoyable.|
|embryonic|ADJ-GRADED早期的;处于萌芽阶段的;胚胎期的 An embryonic process, idea, organization, or organism is one at a very early stage in its development.|
|prototype|N-COUNT原型；样品；样本 A prototype is a new type of machine or device which is not yet ready to be made in large numbers and sold.|
|rendition|N-COUNT(剧本、诗歌或音乐作品的)演出，表演，演绎 A rendition of a play, poem, or piece of music is a performance of it.|
|hi-res screen|high-resolution screen"的缩写，指的是高分辨率屏幕|

Finally, we were ready to try to print some text (which was harder than graphics since you had to worry about character generation and layout). I started considering what the Silentype’s initial utterance should be. Being a programmer, the first thing I thought of was “Hello, World!” but I knew we could probably do better than that so I started asking around for suggestions.

|||
|:---|:---|
|layout|N-COUNT布置；设计；布局 The layout of a garden, building, or piece of writing is the way in which the parts of it are arranged.|
|utterance|N-COUNT言辞；言语；言论 Someone's utterances are the things that they say.|

Someone mentioned that the first message ever sent electronically, tapped out in Morse code by Samuel Morse himself on May 24, 1844, was a bible quote, “What Hath God Wrought?”. In homage to both Samuel Morse and Steve Wozniak, we decided that the first official text printed by the printer should be “What Hath Woz Wrought?”. I wrote an Integer Basic program to print it out about 20 times and I saved the print-out for years but unfortunately lost it at some point, after it had mostly faded out anyway.

|||
|:---|:---|
|bible|N-PROPER《圣经》 The Bible is the holy book on which the Jewish and Christian religions are based.|
|quote|N-COUNT引文；引语；语录 A quote from a book, poem, play, or speech is a passage or phrase from it.|
|hath|（have 的第三人称单数的过时形式） 古英语用法 Hath is an old-fashioned third person singular form of the verb 'have'.|
|wrought|VERB引起;造成 If something has wrought a change, it has made it happen.|
|homage|N-UNCOUNT尊敬;崇敬;敬意 Homage is respect shown towards someone or something you admire, or to a person in authority.|
|faded out|PHRASAL VERB淡出;变得不再引人注目(直至完全消失) When something fades out, it slowly becomes less noticeable or less important until it disappears completely.|

I occasionally thought about what Apple marketing was going to call our new printer, but I never heard any discussion about it. I was afraid they would name it something generic, like “Apple Thermal Printer”, so I was pleased when George Johnson, the marketing person assigned to the project, stopped by and told me they had decided to christen it the “Apple Silentype”. As a lifelong punster I approved, even if it wasn’t a reference to the 5th verse of “Tangled Up In Blue” as I hoped.

|||
|:---|:---|
|stopped by|“顺便拜访”、“路过”或“停下来”|
|christen|VERB开始称呼…为;给…取名为 You say that you christen a person, place, or object a particular name if you choose a name for them and start calling them by that name.|
|punster|喜欢说双关语的人，爱说俏皮话的人|

Vic was worried about the possibility of the software crashing while it was printing. It was possible for a thermal element to be inadvertently left on indefinitely, which could potentially ruin the thermal elements or even cause a fire. Vic solved the problem by adding a bit of hardware to cut current to elements that were left on for more than 10 milliseconds. He asked me to write a test to verify that his precaution was working as intended.

|||
|:---|:---|
|inadvertently|ADJ无意的;并非故意的;因疏忽造成的 An inadvertent action is one that you do without realizing what you are doing.|
|left on|持续开启，忘记关闭|
|indefinitely|ADV无限期地 If a situation will continue indefinitely, it will continue for ever or until someone decides to change it or end it.|
|current|N-COUNT电流 An electric current is a flow of electricity through a wire or circuit.|
|precaution|N-COUNT预防措施；防备 A precaution is an action that is intended to prevent something dangerous or unpleasant from happening.|

I wrote code to intentionally leave each thermal element on, to verify that Vic’s safety measure was effective. I was pleased to see that it worked perfectly, but also a little disappointed to miss more exciting behavior if it hadn’t. I thought of something else to try: what if I left an element on for 9.9 milliseconds, before turning it off for only 30 microseconds, then turning it back on again. It would effectively be on for more than 99% of the time while sidestepping Vic’s remedy. I couldn’t resist coding it up to see what would happen, so I fired up the modified test and nervously awaited the results.

|||
|:---|:---|
|intentionally|ADJ故意的;有意的 Something that is intentional is deliberate.|
|sidestepping|VERB回避，规避(问题等) If you sidestep a problem, you avoid discussing it or dealing with it.|
|remedy|N-COUNT(问题的)解决方法，解决良方 A remedy is a successful way of dealing with a problem.|
|resist|VERB按捺;克制;忍住 If you resist doing something, or resist the temptation to do it, you stop yourself from doing it although you would like to do it.|

At first nothing seemed to happen, except for a low volume humming sound emanating from the printer. Suddenly, after about five seconds, the paper started turning a deep, inky black, spreading out from the print-head organically, almost like a liquid, darker than I had ever seen before. I started smelling an acrid odor and noticed there were open flames near the print-head beginning to spread. I quickly reset the Apple II as I smothered the fire with my jacket. The foul smell drew a small crowd but mercifully no fire alarm.

|||
|:---|:---|
|volume|N-UNCOUNT（广播、电视或音响系统的）音量，声量,响度 The volume of a radio, television, or sound system is the loudness of the sound it produces.|
|humming|VERB发出连续而低沉的声音;发嗡嗡声 If something hums, it makes a low continuous noise.|
|emanating|VERB来自(于);(从…)散发出 If something emanates from somewhere, it comes from there.|
|organically|ADJ（变化或发展）逐渐的，自然的，演进的 Organic change or development happens gradually and naturally rather than suddenly.|
|acrid|ADJ-GRADED（气味或味道）辛辣的，苦的，刺激的 An acrid smell or taste is strong and sharp, and usually unpleasant.|
|odor|气味，名声|
|flame|N-VAR火焰;烈焰;火舌 A flame is a hot bright stream of burning gas that comes from something that is burning.|
|smother|VERB将(火)闷熄 If you smother a fire, you cover it with something in order to put it out.|
|foul|ADJ-GRADED难吃的;肮脏的;恶臭的 If you describe something as foul, you mean it is dirty and smells or tastes unpleasant.|
|crowd|N-COUNT-COLL人群;观众 A crowd is a large group of people who have gathered together, for example to watch or listen to something interesting, or to protest about something.|
|mercifully|ADV幸运地;有福气地;幸好 You can use mercifully to show that you are glad that something good has happened, or that something bad has not happened or has stopped.|

Unfortunately, the experiment seemed to permanently damage the print-head; it burned out or possibly melted some of the thermal elements. The printer could no longer print text or graphics, but it still was able to set the paper on fire, so I kept it around for the occasional incendiary demo.

|||
|:---|:---|
|permanently|ADJ永久的；永恒的 Something that is permanent lasts for ever.|
|melt|V-ERG(使)熔化;(使)融化 When a solid substance melts or when you melt it, it changes to a liquid, usually because it has been heated.|
|incendiary|ADJ纵火的;放火的;能引起燃烧的 Incendiary weapons or attacks are ones that cause large fires.|

I finished the Silentype firmware around mid-September, which was theoretically early enough to meet our goal of a Christmas 1979 release, but Trendcom had a series of production issues that delayed shipments in any significant volume until early 1980. It sold pretty well for a while as the official printer for the Apple II, before it was replaced by the ImageWriter dot matrix printer around the end of 1983.

|||
|:---|:---|
|firmware|N-UNCOUNT固件(由于经常使用而储存在芯片上的一组指令) In computer systems, firmware is a set of commands which are stored on a chip rather than as part of a program, because the computer uses them very often.|
|dot matrix printer|点阵打印机|

