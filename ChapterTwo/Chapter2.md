
# Chapter 2. Architectural Thinking

An architect sees things differently from a developer’s point of view, much in the same way a meteorologist might see clouds differently from an artist’s point of view. This is called architectural thinking. Unfortunately, too many architects believe that architectural thinking is simply just “thinking about the architecture.”

Architectural thinking is much more than that. It is seeing things with an architec‐ tural eye, or an architectural point of view. There are four main aspects of thinking like an architect. First, it’s understanding the difference between architecture and design and knowing how to collaborate with development teams to make architecture work. Second, it’s about having a wide breadth of technical knowledge while still maintaining a certain level of technical depth, allowing the architect to see solutions and possibilities that others do not see. Third, it’s about understanding, analyzing, and reconciling trade-offs between various solutions and technologies. Finally, it’s about understanding the importance of business drivers and how they translate to architectural concerns.

In this chapter we explore these four aspects of thinking like an architect and seeing things with an architectural eye.

-----

# فصل ۲. تفکر معماری

یک معمار چیزها را متفاوت از دیدگاه یک توسعه‌دهنده می‌بیند، تقریباً همان‌طور که یک هواشناس ممکن است ابرها را متفاوت از دیدگاه یک هنرمند ببیند. این امر architectural thinking نامیده می‌شود. متأسفانه، بسیاری از معماران بر این باورند که architectural thinking صرفاً «فکر کردن درباره معماری» است.

تا Architectural thinking بسیار بیشتر از آن است. این امر دیدن چیزها با چشم معماری، یا دیدگاه معماری است. چهار جنبه اصلی تفکر مانند یک معمار وجود دارد. اول، درک تفاوت بین architecture و design و دانستن چگونگی همکاری با تیم‌های توسعه برای کارکردن معماری. دوم، داشتن breadth گسترده دانش فنی در حالی که همچنان حفظ سطح معینی از technical depth، که به معمار اجازه می‌دهد راه‌حل‌ها و امکاناتی را ببیند که دیگران نمی‌بینند. سوم، درک، تحلیل، و آشتی دادن trade-offs بین راه‌حل‌ها و فناوری‌های مختلف. در نهایت، درک اهمیت business drivers و چگونگی ترجمه آن‌ها به architectural concerns.

در این فصل، این چهار جنبه تفکر مانند یک معمار و دیدن چیزها با چشم معماری را کاوش می‌کنیم.

-----
## Architecture Versus Design
The difference between architecture and design is often a confusing one. Where does architecture end and design begin? What responsibilities does an architect have ver‐ sus those of a developer? Thinking like an architect is knowing the difference between architecture and design and seeing how the two integrate closely to form solutions to business and technical problems.

Consider Figure 2-1, which illustrates the traditional responsibilities an architect has, as compared to those of a developer. As shown in the diagram, an architect is responsible for things like analyzing business requirements to extract and define the architectural characteristics (“-ilities”), selecting which architecture patterns and styles would fit the problem domain, and creating components (the building blocks of the system). The artifacts created from these activities are then handed off to the develop‐ ment team, which is responsible for creating class diagrams for each component, creating user interface screens, and developing and testing source code.

There are several issues with the traditional responsibility model illustrated in Figure 2-1. As a matter of fact, this illustration shows exactly why architecture rarely works. Specifically, it is the unidirectional arrow passing though the virtual and physical barriers separating the architect from the developer that causes all of the problems associated with architecture. Decisions an architect makes sometimes never make it to the development teams, and decisions development teams make that change the architecture rarely get back to the architect. In this model the architect is disconnected from the development teams, and as such the architecture rarely pro‐ vides what it was originally set out to do.

To make architecture work, both the physical and virtual barriers that exist between architects and developers must be broken down, thus forming a strong bidirectional relationship between architects and development teams. The architect and developer must be on the same virtual team to make this work, as depicted in Figure 2-2. Not only does this model facilitate strong bidirectional communication between architecture and development, but it also allows the architect to provide mentoring and coaching to developers on the team.

Unlike the old-school waterfall approaches to static and rigid software architecture, the architecture of today’s systems changes and evolves every iteration or phase of a project. A tight collaboration between the architect and the development team is essential for the success of any software project. So where does architecture end and design begin? It doesn’t. They are both part of the circle of life within a software project and must always be kept in synchronization with each other in order to succeed.

----
## Architecture Versus Design

تفاوت بین معماری و طراحی اغلب گیج‌کننده است. معماری کجا به پایان می‌رسد و طراحی از کجا آغاز می‌شود؟ مسئولیت‌های یک معمار در مقابل مسئولیت‌های یک توسعه‌دهنده چیست؟ تفکر مانند یک معمار به معنای شناخت تفاوت بین معماری و طراحی و دیدن چگونگی ادغام نزدیک آن دو برای تشکیل راه‌حل‌هایی برای مشکلات تجاری و فنی است.

تا Figure 2-1 را در نظر بگیرید، که مسئولیت‌های سنتی یک معمار را در مقایسه با مسئولیت‌های یک توسعه‌دهنده نشان می‌دهد. همان‌طور که در دیاگرام نشان داده شده است، یک معمار مسئول چیزهایی مانند تحلیل نیازمندی‌های تجاری برای استخراج و تعریف ویژگی‌های معماری («-ilities»)، انتخاب الگوها و سبک‌های معماری که با دامنه مسئله متناسب هستند، و ایجاد components (بلوک‌های ساختمانی سیستم) است. مصنوعات ایجادشده از این فعالیت‌ها سپس به تیم توسعه تحویل داده می‌شود، که مسئول ایجاد class diagrams برای هر component، ایجاد صفحات user interface، و توسعه و آزمون source code است.

چندین مسئله با مدل مسئولیت سنتی نشان‌داده‌شده در Figure 2-1 وجود دارد. در واقع، این تصویر دقیقاً نشان می‌دهد که چرا معماری به ندرت کار می‌کند. به‌طور خاص، این پیکان یک‌جهته است که از طریق موانع مجازی و فیزیکی جداکننده معمار از توسعه‌دهنده عبور می‌کند و باعث تمام مشکلات مرتبط با معماری می‌شود. تصمیماتی که یک معمار می‌گیرد گاهی هرگز به تیم‌های توسعه نمی‌رسد، و تصمیماتی که تیم‌های توسعه می‌گیرند و معماری را تغییر می‌دهند به ندرت به معمار بازمی‌گردد. در این مدل، معمار از تیم‌های توسعه جدا است، و به همین دلیل معماری به ندرت آنچه را که در ابتدا برای آن طراحی شده بود فراهم می‌کند.

برای اینکه معماری کار کند، هم موانع فیزیکی و هم مجازی موجود بین معماران و توسعه‌دهندگان باید شکسته شوند، و بنابراین یک رابطه دوجهته قوی بین معماران و تیم‌های توسعه تشکیل شود. معمار و توسعه‌دهنده باید در یک تیم مجازی یکسان باشند تا این کار موفق شود، همان‌طور که در Figure 2-2 نشان داده شده است. این مدل نه تنها ارتباط دوجهته قوی بین معماری و توسعه را تسهیل می‌کند، بلکه به معمار اجازه می‌دهد تا mentoring و coaching به توسعه‌دهندگان تیم ارائه دهد.

برخلاف رویکردهای waterfall قدیمی‌مدرسه به معماری نرم‌افزاری ایستا و صلب، معماری سیستم‌های امروزی در هر تکرار یا فاز یک پروژه تغییر می‌کند و تکامل می‌یابد. همکاری نزدیک بین معمار و تیم توسعه برای موفقیت هر پروژه نرم‌افزاری ضروری است. بنابراین معماری کجا به پایان می‌رسد و طراحی از کجا آغاز می‌شود؟ اینطور نیست. هر دو بخشی از چرخه حیات درون یک پروژه نرم‌افزاری هستند و باید همیشه با یکدیگر همگام نگه داشته شوند تا موفق شوند.

----
### Technical Breadth

The scope of technological detail differs between developers and architects. Unlike a developer, who must have a significant amount of technical depth to perform their job, a software architect must have a significant amount of technical breadth to think like an architect and see things with an architecture point of view. This is illustrated by the knowledge pyramid shown in Figure 2-3, which encapsulates all the technical knowledge in the world. It turns out that the kind of information a technologist should value differs with career stages.

As shown in Figure 2-3, any individual can partition all their knowledge into three sections: stuff you know, stuff you know you don’t know, and stuff you don’t know you don’t know.

Stuff you know includes the technologies, frameworks, languages, and tools a technologist uses on a daily basis to perform their job, such as knowing Java as a Java programmer. Stuff you know you don’t know includes those things a technologist knows a little about or has heard of but has little or no expertise in. A good example of this level of knowledge is the Clojure programming language. Most technologists have heard of Clojure and know it’s a programming language based on Lisp, but they can’t code in the language. Stuff you don’t know you don’t know is the largest part of the knowledge triangle and includes the entire host of technologies, tools, frameworks, and languages that would be the perfect solution to a problem a technologist is trying to solve, but the technologist doesn’t even know those things exist.

A developer’s early career focuses on expanding the top of the pyramid, to build experience and expertise. This is the ideal focus early on, because developers need more perspective, working knowledge, and hands-on experience. Expanding the top incidentally expands the middle section; as developers encounter more technologies and related artifacts, it adds to their stock of stuff you know you don’t know.

In Figure 2-4, expanding the top of the pyramid is beneficial because expertise is valued. However, the stuff you know is also the stuff you must maintain nothing is static in the software world. If a developer becomes an expert in Ruby on Rails, that expertise won’t last if they ignore Ruby on Rails for a year or two. The things at the top of the pyramid require time investment to maintain expertise. Ultimately, the size of the top of an individual’s pyramid is their technical depth.

However, the nature of knowledge changes as developers transition into the architect role. A large part of the value of an architect is a broad understanding of technology and how to use it to solve particular problems. For example, as an architect, it is more beneficial to know that five solutions exist for a particular problem than to have sin‐ gular expertise in only one. The most important parts of the pyramid for architects are the top and middle sections; how far the middle section penetrates into the bot‐ tom section represents an architect’s technical breadth, as shown in Figure 2-5.

As an architect, breadth is more important than depth. Because architects must make decisions that match capabilities to technical constraints, a broad understanding of a wide variety of solutions is valuable. Thus, for an architect, the wise course of action is to sacrifice some hard-won expertise and use that time to broaden their portfolio, as shown in Figure 2-6. As illustrated in the diagram, some areas of expertise will remain, probably in particularly enjoyable technology areas, while others usefully atrophy.

Our knowledge pyramid illustrates how fundamentally different the role of architect compares to developer. Developers spend their whole careers honing expertise, and transitioning to the architect role means a shift in that perspective, which many individuals find difficult. This in turn leads to two common dysfunctions: first, an architect tries to maintain expertise in a wide variety of areas, succeeding in none of them and working themselves ragged in the process. Second, it manifests as stale expertise —the mistaken sensation that your outdated information is still cutting edge. We see this often in large companies where the developers who founded the company have moved into leadership roles yet still make technology decisions using ancient criteria (see “Frozen Caveman Anti-Pattern” on page 30).

Architects should focus on technical breadth so that they have a larger quiver from which to draw arrows. Developers transitioning to the architect role may have to change the way they view knowledge acquisition. Balancing their portfolio of knowledge regarding depth versus breadth is something every developer should consider throughout their career

----
### Technical Breadth

دامنه جزئیات فناوری بین توسعه‌دهندگان و معماران متفاوت است. برخلاف یک توسعه‌دهنده، که باید مقدار قابل توجهی عمق فنی برای انجام کار خود داشته باشد، یک معمار نرم‌افزار باید مقدار قابل توجهی breadth فنی داشته باشد تا مانند یک معمار فکر کند و چیزها را با دیدگاه معماری ببیند. این امر توسط هرم دانش نشان‌داده‌شده در Figure 2-3 نشان داده می‌شود، که تمام دانش فنی جهان را در بر می‌گیرد. معلوم می‌شود که نوع اطلاعاتی که یک متخصص فناوری باید ارزش‌گذاری کند با مراحل شغلی متفاوت است.

همان‌طور که در Figure 2-3 نشان داده شده است، هر فرد می‌تواند تمام دانش خود را به سه بخش تقسیم کند: چیزهایی که می‌دانید، چیزهایی که می‌دانید نمی‌دانید، و چیزهایی که نمی‌دانید نمی‌دانید.

چیزهایی که می‌دانید شامل فناوری‌ها، فریم‌ورک‌ها، زبان‌ها، و ابزارهایی است که یک متخصص فناوری روزانه برای انجام کار خود استفاده می‌کند، مانند دانستن Java به عنوان یک برنامه‌نویس Java. چیزهایی که می‌دانید نمی‌دانید شامل چیزهایی است که یک متخصص فناوری کمی درباره آن‌ها می‌داند یا شنیده است اما تخصص کم یا هیچی در آن‌ها ندارد. مثال خوبی از این سطح دانش زبان برنامه‌نویسی Clojure است. اکثر متخصصان فناوری درباره Clojure شنیده‌اند و می‌دانند که یک زبان برنامه‌نویسی مبتنی بر Lisp است، اما نمی‌توانند در آن زبان کدنویسی کنند. چیزهایی که نمی‌دانید نمی‌دانید بزرگ‌ترین بخش مثلث دانش است و شامل کل مجموعه فناوری‌ها، ابزارها، فریم‌ورک‌ها، و زبان‌هایی است که راه‌حل عالی برای مشکلی که یک متخصص فناوری در حال حل آن است خواهند بود، اما متخصص فناوری حتی نمی‌داند که آن‌ها وجود دارند.

اوایل حرفه یک توسعه‌دهنده بر گسترش بالای هرم تمرکز دارد، تا تجربه و تخصص بسازد. این تمرکز ایده‌آل در ابتدا است، زیرا توسعه‌دهندگان به دیدگاه بیشتر، دانش عملی، و تجربه عملی نیاز دارند. گسترش بالا به طور اتفاقی بخش میانی را گسترش می‌دهد؛ همان‌طور که توسعه‌دهندگان با فناوری‌های بیشتر و مصنوعات مرتبط روبرو می‌شوند، به ذخیره چیزهایی که می‌دانید نمی‌دانید اضافه می‌کند.

در Figure 2-4، گسترش بالای هرم مفید است زیرا تخصص ارزشمند است. با این حال، چیزهایی که می‌دانید همچنین چیزهایی هستند که باید حفظ شوند هیچ چیز در جهان نرم‌افزار ایستا نیست. اگر یک توسعه‌دهنده متخصص در Ruby on Rails شود، آن تخصص دوام نخواهد آورد اگر Ruby on Rails را برای یک یا دو سال نادیده بگیرد. چیزهای بالای هرم نیازمند سرمایه‌گذاری زمان برای حفظ تخصص هستند. در نهایت، اندازه بالای هرم فرد عمق فنی او است.

با این حال، طبیعت دانش تغییر می‌کند همان‌طور که توسعه‌دهندگان به نقش معمار منتقل می‌شوند. بخش بزرگی از ارزش یک معمار درک گسترده از فناوری و چگونگی استفاده از آن برای حل مشکلات خاص است. برای مثال، به عنوان یک معمار، مفیدتر است که بدانید پنج راه‌حل برای یک مشکل خاص وجود دارد تا اینکه تخصص singular تنها در یکی داشته باشید. مهم‌ترین بخش‌های هرم برای معماران بخش‌های بالا و میانی هستند؛ اینکه بخش میانی تا چه حد به بخش پایین نفوذ کند breadth فنی یک معمار را نشان می‌دهد، همان‌طور که در Figure 2-5 نشان داده شده است.

به عنوان یک معمار، breadth مهم‌تر از depth است. زیرا معماران باید تصمیماتی بگیرند که قابلیت‌ها را با محدودیت‌های فنی تطبیق دهند، درک گسترده از مجموعه وسیعی از راه‌حل‌ها ارزشمند است. بنابراین، برای یک معمار، مسیر عاقلانه این است که برخی از تخصص‌های سخت‌کسب‌شده را قربانی کند و از آن زمان برای گسترش پرتفولیو خود استفاده کند، همان‌طور که در Figure 2-6 نشان داده شده است. همان‌طور که در نمودار نشان داده شده است، برخی حوزه‌های تخصص باقی خواهند ماند، احتمالاً در حوزه‌های فناوری لذت‌بخش خاص، در حالی که دیگران به طور مفید atrophy می‌کنند.

هرم دانش ما نشان می‌دهد که نقش معمار چقدر اساساً متفاوت از توسعه‌دهنده است. توسعه‌دهندگان کل حرفه خود را صرف honing تخصص می‌کنند، و انتقال به نقش معمار به معنای تغییر در آن دیدگاه است، که بسیاری از افراد آن را دشوار می‌یابند. این امر به نوبه خود به دو dysfunction رایج منجر می‌شود: اول، یک معمار سعی می‌کند تخصص در مجموعه وسیعی از حوزه‌ها حفظ کند، در هیچ‌کدام موفق نمی‌شود و خود را در فرآیند خسته می‌کند. دوم، آن به عنوان تخصص stale ظاهر می‌شود —احساس اشتباه‌آمیز اینکه اطلاعات قدیمی شما هنوز cutting edge است. ما این را اغلب در شرکت‌های بزرگ می‌بینیم جایی که توسعه‌دهندگان بنیان‌گذار شرکت به نقش‌های رهبری منتقل شده‌اند اما همچنان تصمیمات فناوری را با استفاده از معیارهای ancient می‌گیرند (رجوع شود به “Frozen Caveman Anti-Pattern” در صفحه ۳۰).

معماران باید بر breadth فنی تمرکز کنند تا تیرکمان بزرگ‌تری داشته باشند که از آن تیرها بکشند. توسعه‌دهندگان در حال انتقال به نقش معمار ممکن است مجبور باشند نحوه دیدگاه خود به کسب دانش را تغییر دهند. تعادل پرتفولیو دانش خود در مورد depth در مقابل breadth چیزی است که هر توسعه‌دهنده باید در طول حرفه خود در نظر بگیرد.

----
Frozen Caveman Anti-Pattern

A behavioral anti-pattern commonly observed in the wild, the Frozen Caveman AntiPattern, describes an architect who always reverts back to their pet irrational concern for every architecture. For example, one of Neal’s colleagues worked on a system that featured a centralized architecture. Yet, each time they delivered the design to the client architects, the persistent question was “But what if we lose Italy?” Several years before, a freak communication problem had prevented headquarters from communicating with its stores in Italy, causing great inconvenience. While the chances of a reoccurrence were extremely small, the architects had become obsessed about this particular architectural characteristic.

Generally, this anti-pattern manifests in architects who have been burned in the past by a poor decision or unexpected occurrence, making them particularly cautious in the future. While risk assessment is important, it should be realistic as well. Understanding the difference between genuine versus perceived technical risk is part of the ongoing learning process for architects. Thinking like an architect requires overcoming these “frozen caveman” ideas and experiences, seeing other solutions, and asking more relevant questions.

----
### الگوی ضدمعماری Frozen Caveman

یک الگوی ضدمعماری رفتاری که به‌طور رایج در عمل مشاهده می‌شود، Frozen Caveman Anti-Pattern، معمارانی را توصیف می‌کند که همواره در هر معماری به نگرانی غیرمنطقی مورد علاقه خود بازمی‌گردند. برای مثال، یکی از همکاران Neal بر روی سیستمی کار می‌کرد که دارای یک centralized architecture بود. با این حال، هر بار که طرح را به معماران مشتری تحویل می‌دادند، پرسش مداوم این بود: «اما اگر ایتالیا را از دست بدهیم چه می‌شود؟» چند سال پیش، یک مشکل ارتباطی غیرعادی مانع از ارتباط مقر اصلی با فروشگاه‌هایش در ایتالیا شده بود و باعث ناراحتی زیادی شده بود. در حالی که شانس تکرار چنین رخدادی بسیار کم بود، معماران نسبت به این ویژگی معماری خاص وسواس پیدا کرده بودند.

به‌طور کلی، این anti-pattern در معمارانی ظاهر می‌شود که در گذشته بر اثر یک تصمیم ضعیف یا رخداد غیرمنتظره آسیب دیده‌اند و این امر آن‌ها را در آینده به‌طور خاص محتاط می‌کند. در حالی که ارزیابی ریسک مهم است، باید واقع‌بینانه نیز باشد. درک تفاوت بین ریسک فنی واقعی در مقابل ریسک ادراکی بخشی از فرآیند یادگیری مداوم برای معماران است. تفکر مانند یک معمار مستلزم غلبه بر این ایده‌ها و تجربیات «frozen caveman»، دیدن راه‌حل‌های دیگر، و مطرح کردن پرسش‌های مرتبط‌تر است.

-----

Analyzing Trade-Offs

Thinking like an architect is all about seeing trade-offs in every solution, technical or otherwise, and analyzing those trade-offs to determine what is the best solution. To quote Mark (one of your authors):

Architecture is the stuff you can’t Google.

Everything in architecture is a trade-off, which is why the famous answer to every architecture question in the universe is “it depends.” While many people get increasingly annoyed at this answer, it is unfortunately true. You cannot Google the answer to whether REST or messaging would be better, or whether microservices is the right architecture style, because it does depend. It depends on the deployment environment, business drivers, company culture, budgets, timeframes, developer skill set, and dozens of other factors. Everyone’s environment, situation, and problem is different, hence why architecture is so hard. To quote Neal (another one of your authors):

There are no right or wrong answers in architecture only trade-offs.

For example, consider an item auction system, as illustrated in Figure 2-7, where someone places a bid for an item up for auction.

The Bid Producer service generates a bid from the bidder and then sends that bid amount to the Bid Capture, Bid Tracking, and Bid Analytics services. This could be done by using queues in a point-to-point messaging fashion or by using a topic in a publish-and-subscribe messaging fashion. Which one should the architect use? You can’t Google the answer. Architectural thinking requires the architect to analyze the trade-offs associated with each option and select the best one given the specific situation.

The two messaging options for the item auction system are shown in Figures 2-8 and 2-9, with Figure 2-8 illustrating the use of a topic in a publish-and-subscribe messaging model, and Figure 2-9 illustrating the use of queues in a point-to-point messaging model.

The clear advantage (and seemingly obvious solution) to this problem in Figure 2-8 is that of architectural extensibility. The Bid Producer service only requires a single connection to a topic, unlike the queue solution in Figure 2-9 where the Bid Producer needs to connect to three different queues. If a new service called Bid History were to be added to this system due to the requirement to provide each bidder with a history of all the bids they made in each auction, no changes at all would be needed to the existing system. When the new Bid History service is created, it could simply subscribe to the topic already containing the bid information. In the queue option shown in Figure 2-9, however, a new queue would be required for the Bid History service, and the Bid Producer would need to be modified to add an additional connection to the new queue. The point here is that using queues requires significant change to the system when adding new bidding functionality, whereas with the topic approach no changes are needed at all in the existing infrastructure. Also, notice that the Bid Producer is more decoupled in the topic option—the Bid Producer doesn’t know how the bidding information will be used or by which services. In the queue option the Bid Producer knows exactly how the bidding information is used (and by whom), and hence is more coupled to the system.

With this analysis it seems clear that the topic approach using the publish and subscribe messaging model is the obvious and best choice. However, to quote Rich Hickey, the creator of the Clojure programming language:

Programmers know the benefits of everything and the trade-offs of nothing. Architects need to understand both.

Thinking architecturally is looking at the benefits of a given solution, but also analyzing the negatives, or trade-offs, associated with a solution. Continuing with the auction system example, a software architect would analyze the negatives of the topic solution. In analyzing the differences, notice first in Figure 2-8 that with a topic, any‐ one can access bidding data, which introduces a possible issue with data access and data security. In the queue model illustrated in Figure 2-9, the data sent to the queue can only be accessed by the specific consumer receiving that message. If a rogue ser‐ vice did listen in on a queue, those bids would not be received by the corresponding service, and a notification would immediately be sent about the loss of data (and hence a possible security breach). In other words, it is very easy to wiretap into a topic, but not a queue.

In addition to the security issue, the topic solution in Figure 2-8 only supports homogeneous contracts. All services receiving the bidding data must accept the same con‐ tract and set of bidding data. In the queue option in Figure 2-9, each consumer can have its own contract specific to the data it needs. For example, suppose the new Bid History service requires the current asking price along with the bid, but no other ser‐ vice needs that information. In this case, the contract would need to be modified, impacting all other services using that data. In the queue model, this would be a separate channel, hence a separate contract not impacting any other service.

Another disadvantage of the topic model illustrated in Figure 2-8 is that it does not support monitoring of the number of messages in the topic and hence auto-scaling capabilities. However, with the queue option in Figure 2-9, each queue can be moni‐ tored individually, and programmatic load balancing applied to each bidding con‐ sumer so that each can be automatically scaled independency from one another. Note that this trade-off is technology specific in that the Advanced Message Queuing Pro‐ tocol (AMQP) can support programmatic load balancing and monitoring because of the separation between an exchange (what the producer sends to) and a queue (what the consumer listens to).

Given this trade-off analysis, now which is the better option? And the answer? It depends! Table 2-1 summarizes these trade-offs.


The point here is that everything in software architecture has a trade-off: an advantage and disadvantage. Thinking like an architect is analyzing these trade-offs, then asking “which is more important: extensibility or security?” The decision between different solutions will always depend on the business drivers, environment, and a host of other factors.

----
### تحلیل موازنه‌ها

تفکر مانند یک معمار کاملاً مربوط به دیدن موازنه‌ها در هر راهکار، چه فنی و چه غیر آن، و تحلیل این موازنه‌ها برای تعیین بهترین راه‌حل است. به نقل از Mark (یکی از نویسندگان کتاب شما):

Architecture is the stuff you can’t Google.

هر چیز در معماری یک موازنه است، به همین دلیل پاسخ مشهور به هر سؤال معماری در جهان این است که «بستگی دارد». گرچه بسیاری از افراد با شنیدن این پاسخ روزبه‌روز کلافه‌تر می‌شوند، اما متأسفانه این پاسخ درست است. شما نمی‌توانید پاسخ این را که آیا REST یا messaging بهتر است، یا اینکه microservices سبک معماری مناسبی است، در گوگل پیدا کنید، زیرا واقعاً بستگی دارد. این موضوع بستگی به محیط استقرار، محرک‌های تجاری، فرهنگ شرکت، بودجه‌ها، زمان‌بندی‌ها، مجموعه مهارت‌های توسعه‌دهنده، و ده‌ها عامل دیگر دارد. محیط، وضعیت و مسئله هر فرد متفاوت است، از این رو معماری تا این حد دشوار است. به نقل از Neal (یکی دیگر از نویسندگان کتاب شما):

There are no right or wrong answers in architecture only trade-offs.

برای مثال، یک سیستم مزایده کالا را در نظر بگیرید، همان‌طور که در Figure 2-7 نشان داده شده است، جایی که فردی پیشنهادی برای کالایی که در مزایده است ثبت می‌کند.

سرویس Bid Producer پیشنهادی از مزایده‌گذار تولید می‌کند و سپس مبلغ آن پیشنهاد را به سرویس‌های Bid Capture، Bid Tracking، و Bid Analytics ارسال می‌کند. این کار می‌تواند با استفاده از queues در شیوه پیام‌رسانی point-to-point یا با استفاده از یک topic در شیوه پیام‌رسانی publish-and-subscribe انجام شود. معمار باید از کدام استفاده کند؟ شما نمی‌توانید پاسخ را در گوگل پیدا کنید. تفکر معماری مستلزم آن است که معمار موازنه‌های مرتبط با هر گزینه را تحلیل کند و بهترین گزینه را با توجه به وضعیت خاص انتخاب کند.

دو گزینه پیام‌رسانی برای سیستم مزایده کالا در Figures 2-8 و 2-9 نشان داده شده‌اند، که Figure 2-8 استفاده از یک topic در مدل پیام‌رسانی publish-and-subscribe را نشان می‌دهد، و Figure 2-9 استفاده از queues در مدل پیام‌رسانی point-to-point را نشان می‌دهد.

مزیت آشکار (و به ظاهر راه‌حل بدیهی) برای این مسئله در Figure 2-8 قابلیت توسعه‌پذیری معماری است. سرویس Bid Producer تنها به یک اتصال به یک topic نیاز دارد، برخلاف راه‌حل queue در Figure 2-9 که در آن Bid Producer باید به سه queue متفاوت متصل شود. اگر سرویس جدیدی به نام Bid History به این سیستم اضافه شود به دلیل الزام ارائه تاریخچه تمام پیشنهادهایی که هر مزایده‌گذار در هر مزایده انجام داده است، هیچ تغییری در سیستم موجود لازم نخواهد بود. هنگامی که سرویس Bid History جدید ایجاد شود، می‌تواند به سادگی به topic که از قبل حاوی اطلاعات پیشنهاد است اشتراک کند. با این حال، در گزینه queue نشان‌داده‌شده در Figure 2-9، یک queue جدید برای سرویس Bid History لازم خواهد بود، و Bid Producer باید تغییر یابد تا اتصال اضافی به queue جدید اضافه شود. نکته اینجا این است که استفاده از queues نیازمند تغییر قابل توجه در سیستم هنگام افزودن عملکرد مزایده جدید است، در حالی که با رویکرد topic هیچ تغییری در زیرساخت موجود لازم نیست. همچنین، توجه کنید که Bid Producer در گزینه topic بیشتر decoupled است—Bid Producer نمی‌داند اطلاعات مزایده چگونه استفاده خواهد شد یا توسط کدام سرویس‌ها. در گزینه queue، Bid Producer دقیقاً می‌داند اطلاعات مزایده چگونه استفاده می‌شود (و توسط چه کسانی)، و بنابراین بیشتر به سیستم coupled است.

با این تحلیل به نظر می‌رسد رویکرد topic با استفاده از مدل پیام‌رسانی publish and subscribe انتخاب بدیهی و بهترین است. با این حال، به نقل از Rich Hickey، خالق زبان برنامه‌نویسی Clojure:

Programmers know the benefits of everything and the trade-offs of nothing. Architects need to understand both.

تفکر معماری نگاه کردن به مزایای یک راه‌حل داده‌شده است، اما همچنین تحلیل منفی‌ها، یا موازنه‌ها، مرتبط با یک راه‌حل. ادامه مثال سیستم مزایده، یک معمار نرم‌افزار منفی‌های راه‌حل topic را تحلیل می‌کند. در تحلیل تفاوت‌ها، ابتدا در Figure 2-8 توجه کنید که با یک topic، هر کسی می‌تواند به داده‌های مزایده دسترسی داشته باشد، که این امر مسئله احتمالی در دسترسی به داده و امنیت داده را ایجاد می‌کند. در مدل queue نشان‌داده‌شده در Figure 2-9، داده ارسال‌شده به queue تنها می‌تواند توسط مصرف‌کننده خاصی که آن پیام را دریافت می‌کند دسترسی یابد. اگر یک سرویس سرکش بر روی یک queue شنود کند، آن پیشنهادها توسط سرویس مربوطه دریافت نخواهد شد، و اعلانی بلافاصله درباره از دست رفتن داده (و بنابراین نقض امنیتی احتمالی) ارسال خواهد شد. به عبارت دیگر، شنود در یک topic بسیار آسان است، اما در یک queue نه.

علاوه بر مسئله امنیتی، راه‌حل topic در Figure 2-8 تنها از homogeneous contracts پشتیبانی می‌کند. تمام سرویس‌های دریافت‌کننده داده‌های مزایده باید همان contract و مجموعه داده‌های مزایده را بپذیرند. در گزینه queue در Figure 2-9، هر مصرف‌کننده می‌تواند contract خاص خود را متناسب با داده‌هایی که نیاز دارد داشته باشد. برای مثال، فرض کنید سرویس Bid History جدید نیازمند قیمت درخواستی فعلی همراه با پیشنهاد است، اما هیچ سرویس دیگری به آن اطلاعات نیاز ندارد. در این مورد، contract باید تغییر یابد، که بر تمام سرویس‌های دیگر استفاده‌کننده از آن داده تأثیر می‌گذارد. در مدل queue، این یک کانال جداگانه خواهد بود، بنابراین یک contract جداگانه که بر هیچ سرویس دیگری تأثیر نمی‌گذارد.

معایب دیگری از مدل topic نشان‌داده‌شده در Figure 2-8 این است که از نظارت بر تعداد پیام‌ها در topic پشتیبانی نمی‌کند و بنابراین قابلیت‌های auto-scaling ندارد. با این حال، با گزینه queue در Figure 2-9، هر queue می‌تواند به طور جداگانه نظارت شود، و load balancing برنامه‌ریزی‌شده بر روی هر مصرف‌کننده مزایده اعمال شود تا هر کدام بتوانند به طور مستقل از یکدیگر به طور خودکار scaled شوند. توجه کنید که این موازنه خاص فناوری است به این معنا که Advanced Message Queuing Protocol (AMQP) می‌تواند از load balancing برنامه‌ریزی‌شده و نظارت پشتیبانی کند به دلیل جداسازی بین یک exchange (آنچه تولیدکننده به آن ارسال می‌کند) و یک queue (آنچه مصرف‌کننده به آن گوش می‌دهد).

با توجه به این تحلیل موازنه، اکنون کدام گزینه بهتر است؟ و پاسخ؟ بستگی دارد! Table 2-1 این موازنه‌ها را خلاصه می‌کند.


نکته اینجا این است که هر چیز در معماری نرم‌افزار یک موازنه دارد: یک مزیت و یک معایب. تفکر مانند یک معمار تحلیل این موازنه‌ها است، سپس پرسیدن اینکه «کدام مهم‌تر است: extensibility یا security؟» تصمیم بین راه‌حل‌های متفاوت همیشه بستگی به محرک‌های تجاری، محیط، و مجموعه‌ای از عوامل دیگر دارد.

---
Understanding Business Drivers
Thinking like an architect is understanding the business drivers that are required for the success of the system and translating those requirements into architecture characteristics (such as scalability, performance, and availability). This is a challenging task that requires the architect to have some level of business domain knowledge and healthy, collaborative relationships with key business stakeholders. We’ve devoted several chapters in the book on this specific topic. In Chapter 4 we define various architecture characteristics. In Chapter 5 we describe ways to identify and qualify architecture characteristics. And in Chapter 6 we describe how to measure each of these characteristics to ensure the business needs of the system are met.

----
### درک محرک‌های تجاری

تفکر مانند یک معمار به معنای درک محرک‌های تجاری‌ای است که برای موفقیت سیستم ضروری هستند و ترجمه این نیازمندی‌ها به ویژگی‌های معماری (مانند scalability، performance، و availability). این کار وظیفه‌ای چالش‌برانگیز است که نیازمند آن است معمار سطحی از دانش دامنه کسب‌وکار و روابط سالم و مشارکتی با ذینفعان کلیدی کسب‌وکار داشته باشد. ما چندین فصل در کتاب را به این موضوع خاص اختصاص داده‌ایم. در فصل ۴ ویژگی‌های معماری مختلف را تعریف می‌کنیم. در فصل ۵ راه‌هایی را برای شناسایی و اعتبارسنجی ویژگی‌های معماری توصیف می‌کنیم. و در فصل ۶ توصیف می‌کنیم چگونه هر یک از این ویژگی‌ها را اندازه‌گیری کنیم تا اطمینان حاصل شود نیازهای کسب‌وکار سیستم برآورده می‌شوند.

----
Balancing Architecture and Hands-On Coding

One of the difficult tasks an architect faces is how to balance hands-on coding with software architecture. We firmly believe that every architect should code and be able to maintain a certain level of technical depth (see “Technical Breadth” on page 25). While this may seem like an easy task, it is sometimes rather difficult to accomplish.

The first tip in striving for a balance between hands-on coding and being a software architect is avoiding the bottleneck trap. The bottleneck trap occurs when the architect has taken ownership of code within the critical path of a project (usually the underlying framework code) and becomes a bottleneck to the team. This happens because the architect is not a full-time developer and therefore must balance between playing the developer role (writing and testing source code) and the architect role (drawing diagrams, attending meetings, and well, attending more meetings).

One way to avoid the bottleneck trap as an effective software architect is to delegate the critical path and framework code to others on the development team and then focus on coding a piece of business functionality (a service or a screen) one to three iterations down the road. Three positive things happen by doing this. First, the architect is gaining hands-on experience writing production code while no longer becoming a bottleneck on the team. Second, the critical path and framework code is distributed to the development team (where it belongs), giving them ownership and a better understanding of the harder parts of the system. Third, and perhaps most important, the architect is writing the same business-related source code as the development team and is therefore better able to identify with the development team in

terms of the pain they might be going through with processes, procedures, and the development environment.

Suppose, however, that the architect is not able to develop code with the development team. How can a software architect still remain hands-on and maintain some level of technical depth? There are four basic ways an architect can still remain hands-on at work without having to “practice coding from home” (although we recommend practicing coding at home as well).

The first way is to do frequent proof of concepts or POCs. This practice not only requires the architect to write source code, but it also helps validate an architecture decision by taking the implementation details into account. For example, if an architect is stuck trying to make a decision between two caching solutions, one effective way to help make this decision is to develop a working example in each caching product and compare the results. This allows the architect to see first-hand the implementation details and the amount of effort required to develop the full solution. It also allows the architect to better compare architectural characteristics such as scalability, performance, or overall fault tolerance of the different caching solutions.

Our advice when doing proof of concept work is that, whenever possible, the architect should write the best production-quality code they can. We recommend this practice for two reasons. First, quite often, throwaway proof-of-concept code goes into the source code repository and becomes the reference architecture or guiding example for others to follow. The last thing an architect would want is for their throwaway, sloppy code to be a representation of their typical work. The second reason is that by writing production-quality proof-of-concept code, the architect gets practice writing quality, well-structured code rather than continually developing bad coding practices.

Another way an architect can remain hands-on is to tackle some of the technical debt stories or architecture stories, freeing the development team up to work on the critical functional user stories. These stories are usually low priority, so if the architect does not have the chance to complete a technical debt or architecture story within a given iteration, it’s not the end of the world and generally does not impact the success of the iteration.

Similarly, working on bug fixes within an iteration is another way of maintaining hands-on coding while helping the development team as well. While certainly not glamorous, this technique allows the architect to identify where issues and weakness may be within the code base and possibly the architecture.

Leveraging automation by creating simple command-line tools and analyzers to help the development team with their day-to-day tasks is another great way to maintain hands-on coding skills while making the development team more effective. Look for repetitive tasks the development team performs and automate the process. The development team will be grateful for the automation. Some examples are automated source validators to help check for specific coding standards not found in other lint tests, automated checklists, and repetitive manual code refactoring tasks.

Automation can also be in the form of architectural analysis and fitness functions to ensure the vitality and compliance of the architecture. For example, an architect can write Java code in Arch Unit in the Java platform to automate architectural compliance, or write custom fitness functions to ensure architectural compliance while gaining hands-on experience. We talk about these techniques in Chapter 6.

A final technique to remain hands-on as an architect is to do frequent code reviews. While the architect is not actually writing code, at least they are involved in the source code. Further, doing code reviews has the added benefits of being able to ensure compliance with the team

---
### Balancing Architecture and Hands-On Coding

یکی از وظایف دشواری که یک معمار با آن مواجه است، چگونگی برقراری تعادل بین کدنویسی عملی و معماری نرم‌افزار است. ما قویاً بر این باوریم که هر معمار باید کدنویسی کند و بتواند سطح معینی از عمق فنی را حفظ کند (رجوع شود به “Technical Breadth” در صفحه ۲۵). گرچه این امر ممکن است ساده به نظر برسد، اما گاهی اوقات دستیابی به آن کاملاً دشوار است.

اولین نکته در تلاش برای برقراری تعادل بین کدنویسی عملی و نقش معماری نرم‌افزار، اجتناب از تله گلوگاه است. تله گلوگاه زمانی رخ می‌دهد که معمار مالکیت کد درون مسیر حیاتی یک پروژه (معمولاً کد فریم‌ورک زیربنایی) را بر عهده می‌گیرد و به گلوگاه تیم تبدیل می‌شود. این اتفاق به این دلیل رخ می‌دهد که معمار توسعه‌دهنده تمام‌وقت نیست و بنابراین باید بین نقش توسعه‌دهنده (نوشتن و آزمون کد منبع) و نقش معمار (ترسیم نمودارها، حضور در جلسات، و خوب، حضور در جلسات بیشتر) تعادل برقرار کند.

یکی از راه‌های اجتناب از تله گلوگاه به عنوان یک معمار نرم‌افزار مؤثر، واگذاری کد مسیر حیاتی و فریم‌ورک به دیگران در تیم توسعه و سپس تمرکز بر کدنویسی یک قطعه از عملکرد کسب‌وکار (یک سرویس یا یک صفحه) یک تا سه تکرار جلوتر است. با انجام این کار، سه اتفاق مثبت رخ می‌دهد. اول، معمار تجربه عملی در نوشتن کد تولیدی به دست می‌آورد در حالی که دیگر به گلوگاه تیم تبدیل نمی‌شود. دوم، کد مسیر حیاتی و فریم‌ورک به تیم توسعه توزیع می‌شود (که محل مناسب آن همان‌جاست)، و به آن‌ها مالکیت و درک بهتری از بخش‌های سخت‌تر سیستم می‌دهد. سوم، و شاید مهم‌ترین، معمار همان کد منبع مرتبط با کسب‌وکار را می‌نویسد که تیم توسعه می‌نویسد و بنابراین بهتر می‌تواند با تیم توسعه همذات‌پنداری کند در مورد دردهایی که ممکن است با فرآیندها، رویه‌ها، و محیط توسعه مواجه باشند.

فرض کنید، با این حال، که معمار قادر به توسعه کد با تیم توسعه نیست. چگونه یک معمار نرم‌افزار همچنان می‌تواند عملی بماند و سطحی از عمق فنی را حفظ کند؟ چهار راه اساسی وجود دارد که یک معمار می‌تواند همچنان عملی بماند در محل کار بدون نیاز به “تمرین کدنویسی از خانه” (گرچه ما توصیه می‌کنیم تمرین کدنویسی در خانه نیز انجام شود).

اولین راه، انجام مکرر proof of concepts یا POCs است. این عمل نه تنها معمار را ملزم به نوشتن کد منبع می‌کند، بلکه همچنین کمک می‌کند تا تصمیم معماری با در نظر گرفتن جزئیات پیاده‌سازی اعتبار یابد. برای مثال، اگر معمار در تصمیم‌گیری بین دو راهکار caching گیر کرده باشد، یکی از راه‌های مؤثر برای کمک به این تصمیم، توسعه یک نمونه کاری در هر محصول caching و مقایسه نتایج است. این امر به معمار اجازه می‌دهد جزئیات پیاده‌سازی و میزان تلاش لازم برای توسعه راهکار کامل را از نزدیک ببیند. همچنین به معمار اجازه می‌دهد ویژگی‌های معماری مانند scalability، performance، یا fault tolerance کلی راهکارهای caching مختلف را بهتر مقایسه کند.

توصیه ما هنگام انجام کار proof of concept این است که، هر زمان ممکن باشد، معمار بهترین کد با کیفیت تولیدی ممکن را بنویسد. ما این عمل را به دو دلیل توصیه می‌کنیم. اول، اغلب اوقات، کد proof-of-concept دورریختنی وارد مخزن کد منبع می‌شود و به عنوان معماری مرجع یا مثال راهنما برای دیگران تبدیل می‌شود. آخرین چیزی که یک معمار می‌خواهد این است که کد دورریختنی و نامرتب او نمایانگر کار معمول او باشد. دلیل دوم این است که با نوشتن کد proof-of-concept با کیفیت تولیدی، معمار تمرین نوشتن کد با کیفیت و ساختار مناسب را انجام می‌دهد به جای توسعه مداوم عادت‌های کدنویسی بد.

راه دیگری که یک معمار می‌تواند عملی بماند، پرداختن به برخی از داستان‌های بدهی فنی یا داستان‌های معماری است، که تیم توسعه را آزاد می‌کند تا روی داستان‌های کاربری عملکردی حیاتی کار کنند. این داستان‌ها معمولاً اولویت پایینی دارند، بنابراین اگر معمار فرصتی برای تکمیل یک داستان بدهی فنی یا معماری در یک تکرار معین نداشته باشد، پایان جهان نیست و عموماً بر موفقیت تکرار تأثیر نمی‌گذارد.

به طور مشابه، کار روی رفع باگ‌ها درون یک تکرار راه دیگری برای حفظ کدنویسی عملی است در حالی که به تیم توسعه نیز کمک می‌کند. گرچه این کار قطعاً جذاب نیست، اما این تکنیک به معمار اجازه می‌دهد جایی که مشکلات و ضعف‌ها ممکن است در پایگاه کد و احتمالاً معماری وجود داشته باشد را شناسایی کند.

بهره‌برداری از automation با ایجاد ابزارهای ساده خط فرمان و تحلیل‌گرها برای کمک به تیم توسعه در وظایف روزمره‌شان راه عالی دیگری برای حفظ مهارت‌های کدنویسی عملی است در حالی که تیم توسعه را مؤثرتر می‌کند. به دنبال وظایف تکراری که تیم توسعه انجام می‌دهد باشید و فرآیند را خودکار کنید. تیم توسعه از automation سپاسگزار خواهد بود. برخی مثال‌ها عبارتند از ولیداتورهای منبع خودکار برای کمک به بررسی استانداردهای کدنویسی خاص که در آزمون‌های lint دیگر یافت نمی‌شوند، چک‌لیست‌های خودکار، و وظایف ریفکتورینگ کد دستی تکراری.

تا Automation همچنین می‌تواند به شکل تحلیل معماری و fitness functions برای اطمینان از حیات و رعایت معماری باشد. برای مثال، یک معمار می‌تواند کد Java در ArchUnit در پلتفرم Java بنویسد تا رعایت معماری را خودکار کند، یا fitness functions سفارشی بنویسد تا رعایت معماری را اطمینان دهد در حالی که تجربه عملی به دست می‌آورد. ما درباره این تکنیک‌ها در فصل ۶ صحبت می‌کنیم.

یک تکنیک نهایی برای عملی ماندن به عنوان معمار، انجام بازبینی‌های کد مکرر است. گرچه معمار در واقع کد نمی‌نویسد، حداقل در کد منبع درگیر است. علاوه بر این، انجام بازبینی‌های کد مزایای اضافی مانند توانایی اطمینان از رعایت با تیم دارد.