
# Chapter 2. Architectural Thinking

An architect sees things differently from a developer’s point of view, much in the same way a meteorologist might see clouds differently from an artist’s point of view. This is called architectural thinking. Unfortunately, too many architects believe that architectural thinking is simply just “thinking about the architecture.”

Architectural thinking is much more than that. It is seeing things with an architec‐ tural eye, or an architectural point of view. There are four main aspects of thinking like an architect. First, it’s understanding the difference between architecture and design and knowing how to collaborate with development teams to make architecture work. Second, it’s about having a wide breadth of technical knowledge while still maintaining a certain level of technical depth, allowing the architect to see solutions and possibilities that others do not see. Third, it’s about understanding, analyzing, and reconciling trade-offs between various solutions and technologies. Finally, it’s about understanding the importance of business drivers and how they translate to architectural concerns.

In this chapter we explore these four aspects of thinking like an architect and seeing things with an architectural eye.

-----

## فصل ۲. تفکر معماری

یک معمار مسائل را متفاوت از نقطه‌نظر یک توسعه‌دهنده می‌بیند، بسیار شبیه به روشی که یک هواشناس ممکن است ابرها را متفاوت از نقطه‌نظر یک هنرمند ببیند. این «تفکر معماری» (architectural thinking) نامیده می‌شود. متأسفانه، معماران بسیار زیادی معتقدند که تفکر معماری صرفاً «فکر کردن درباره معماری» است.

تفکر معماری بسیار فراتر از آن است. این یعنی دیدن مسائل با یک «چشم معماری» (architectural eye)، یا یک نقطه‌نظر معماری. چهار جنبه اصلی برای فکر کردن مانند یک معمار وجود دارد. اول، درک تفاوت بین معماری (architecture) و طراحی (design) و دانستن چگونگی همکاری با تیم‌های توسعه برای کارآمد ساختن معماری است. دوم، مربوط به داشتن وسعت گسترده‌ای از دانش فنی و در عین حال حفظ سطح معینی از عمق فنی است که به معمار اجازه می‌دهد راه‌حل‌ها و امکاناتی را ببیند که دیگران نمی‌بینند. سوم، مربوط به درک، تحلیل و تطبیق بده‌بستان‌ها (trade-offs) بین راه‌حل‌ها و فناوری‌های مختلف است. در نهایت، مربوط به درک اهمیت محرک‌های تجاری (business drivers) و چگونگی ترجمه آن‌ها به دغدغه‌های معماری (architectural concerns) است.

در این فصل ما این چهار جنبه از فکر کردن مانند یک معمار و دیدن مسائل با یک چشم معماری را بررسی می‌کنیم.

-----
## Architecture Versus Design
The difference between architecture and design is often a confusing one. Where does architecture end and design begin? What responsibilities does an architect have ver‐ sus those of a developer? Thinking like an architect is knowing the difference between architecture and design and seeing how the two integrate closely to form solutions to business and technical problems.

Consider Figure 2-1, which illustrates the traditional responsibilities an architect has, as compared to those of a developer. As shown in the diagram, an architect is responsible for things like analyzing business requirements to extract and define the architectural characteristics (“-ilities”), selecting which architecture patterns and styles would fit the problem domain, and creating components (the building blocks of the system). The artifacts created from these activities are then handed off to the develop‐ ment team, which is responsible for creating class diagrams for each component, creating user interface screens, and developing and testing source code.

There are several issues with the traditional responsibility model illustrated in Figure 2-1. As a matter of fact, this illustration shows exactly why architecture rarely works. Specifically, it is the unidirectional arrow passing though the virtual and physical barriers separating the architect from the developer that causes all of the problems associated with architecture. Decisions an architect makes sometimes never make it to the development teams, and decisions development teams make that change the architecture rarely get back to the architect. In this model the architect is disconnected from the development teams, and as such the architecture rarely pro‐ vides what it was originally set out to do.

To make architecture work, both the physical and virtual barriers that exist between architects and developers must be broken down, thus forming a strong bidirectional relationship between architects and development teams. The architect and developer must be on the same virtual team to make this work, as depicted in Figure 2-2. Not only does this model facilitate strong bidirectional communication between architecture and development, but it also allows the architect to provide mentoring and coaching to developers on the team.

Unlike the old-school waterfall approaches to static and rigid software architecture, the architecture of today’s systems changes and evolves every iteration or phase of a project. A tight collaboration between the architect and the development team is essential for the success of any software project. So where does architecture end and design begin? It doesn’t. They are both part of the circle of life within a software project and must always be kept in synchronization with each other in order to succeed.

----
## معماری در برابر طراحی

تفاوت بین معماری (architecture) و طراحی (design) اغلب گیج‌کننده است. معماری کجا تمام می‌شود و طراحی از کجا شروع می‌شود؟ یک معمار در برابر یک توسعه‌دهنده چه مسئولیت‌هایی دارد؟ فکر کردن مانند یک معمار یعنی دانستن تفاوت بین معماری و طراحی و دیدن اینکه چگونه این دو به طور نزدیک با یکدیگر ادغام می‌شوند تا راه‌حل‌هایی برای مسائل تجاری و فنی شکل دهند.

![Figure2-1](Figure2-1.png)

![Figure2-2](Figure2-2.png)

شکل ۲-۱ را در نظر بگیرید که مسئولیت‌های سنتی یک معمار را در مقایسه با مسئولیت‌های یک توسعه‌دهنده نشان می‌دهد. همانطور که در نمودار نشان داده شده است، یک معمار مسئول مواردی مانند تحلیل نیازمندی‌های تجاری (business requirements) برای استخراج و تعریف ویژگی‌های معماری («-ilities»)، انتخاب الگوهای معماری (architecture patterns) و سبک‌هایی (styles) که با دامنه مسئله (problem domain) متناسب باشند، و ایجاد اجزاء (components) (بلوک‌های سازنده سیستم) است. مصنوعات (artifacts) ایجاد شده از این فعالیت‌ها سپس به تیم توسعه (development team) تحویل داده می‌شود، که مسئول ایجاد نمودارهای کلاس (class diagrams) برای هر جزء، ایجاد صفحات رابط کاربری (user interface screens)، و توسعه و تست کد منبع (source code) است.

چندین مسئله با مدل مسئولیت سنتی که در شکل ۲-۱ نشان داده شده است وجود دارد. در واقع، این تصویر دقیقاً نشان می‌دهد که چرا معماری به ندرت کار می‌کند. به طور خاص، این فلش یک‌طرفه (unidirectional arrow) است که از میان موانع مجازی و فیزیکی (virtual and physical barriers) جداکننده معمار از توسعه‌دهنده عبور می‌کند و باعث تمام مشکلات مرتبط با معماری می‌شود. تصمیماتی که یک معمار می‌گیرد گاهی اوقات هرگز به تیم‌های توسعه نمی‌رسد، و تصمیماتی که تیم‌های توسعه می‌گیرند و معماری را تغییر می‌دهد به ندرت به معمار بازمی‌گردد. در این مدل، معمار از تیم‌های توسعه جدا است و به همین دلیل معماری به ندرت آنچه را که در ابتدا برای آن در نظر گرفته شده بود، فراهم می‌کند.

برای کارآمد ساختن معماری، هم موانع فیزیکی و هم مجازی که بین معماران و توسعه‌دهندگان وجود دارد باید شکسته شود، تا یک رابطه قوی دوطرفه (bidirectional relationship) بین معماران و تیم‌های توسعه شکل گیرد. معمار و توسعه‌دهنده باید در یک تیم مجازی (virtual team) باشند تا این کار کند، همانطور که در شکل ۲-۲ به تصویر کشیده شده است. این مدل نه تنها ارتباط قوی دوطرفه بین معماری و توسعه را تسهیل می‌کند، بلکه به معمار اجازه می‌دهد تا به توسعه‌دهندگان تیم، راهنمایی (mentoring) و مربیگری (coaching) ارائه دهد.

برخلاف رویکردهای قدیمی آبشاری (waterfall approaches) به معماری نرم‌افزار ایستا (static) و صلب (rigid)، معماری سیستم‌های امروزی در هر تکرار (iteration) یا فاز (phase) یک پروژه تغییر می‌کند و تکامل می‌یابد. یک همکاری نزدیک بین معمار و تیم توسعه برای موفقیت هر پروژه نرم‌افزاری ضروری است. پس معماری کجا تمام می‌شود و طراحی از کجا شروع می‌شود؟ اینطور نیست. هر دوی آن‌ها بخشی از چرخه حیات (circle of life) در یک پروژه نرم‌افزاری هستند و برای موفقیت باید همیشه با یکدیگر در همگام‌سازی (synchronization) نگه داشته شوند.

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

## وسعت فنی
محدوده جزئیات فناورانه بین توسعه‌دهندگان و معماران متفاوت است. برخلاف یک توسعه‌دهنده، که برای انجام کار خود باید مقدار قابل توجهی عمق فنی (technical depth) داشته باشد، یک معمار نرم‌افزار باید مقدار قابل توجهی وسعت فنی (technical breadth) داشته باشد تا بتواند مانند یک معمار فکر کند و مسائل را با یک نقطه‌نظر معماری ببیند. این موضوع توسط هرم دانش (knowledge pyramid) نشان داده شده در شکل ۲-۳ به تصویر کشیده شده است، که تمام دانش فنی موجود در جهان را در بر می‌گیرد. به نظر می‌رسد نوع اطلاعاتی که یک فناور (technologist) باید برای آن ارزش قائل شود، با مراحل شغلی او متفاوت است.

![Figure2-3](Figure2-3.png)

همانطور که در شکل ۲-۳ نشان داده شده است، هر فردی می‌تواند تمام دانش خود را به سه بخش تقسیم کند: چیزهایی که می‌دانید (stuff you know)، چیزهایی که می‌دانید که نمی‌دانید (stuff you know you don’t know)، و چیزهایی که نمی‌دانید که نمی‌دانید (stuff you don’t know you don’t know).

«چیزهایی که می‌دانید» شامل فناوری‌ها، چارچوب‌ها (frameworks)، زبان‌ها و ابزارهایی است که یک فناور به صورت روزانه برای انجام کار خود از آن‌ها استفاده می‌کند، مانند دانستن جاوا به عنوان یک برنامه‌نویس جاوا. «چیزهایی که می‌دانید که نمی‌دانید» شامل آن چیزهایی است که یک فناور کمی درباره آن‌ها می‌داند یا نامشان را شنیده است اما تخصص کمی در آن‌ها دارد یا اصلاً تخصصی ندارد. یک مثال خوب از این سطح دانش، زبان برنامه‌نویسی Clojure است. اکثر فناوران نام Clojure را شنیده‌اند و می‌دانند که این یک زبان برنامه‌نویسی مبتنی بر Lisp است، اما نمی‌توانند با آن زبان کد بنویسند. «چیزهایی که نمی‌دانید که نمی‌دانید» بزرگترین بخش مثلث دانش است و شامل تمام مجموعه فناوری‌ها، ابزارها، چارچوب‌ها و زبان‌هایی می‌شود که می‌توانستند راه‌حل عالی برای مشکلی باشند که یک فناور در تلاش برای حل آن است، اما آن فناور حتی از وجود آن چیزها خبر ندارد.

مراحل اولیه شغلی یک توسعه‌دهنده بر گسترش بالای هرم تمرکز دارد تا تجربه و تخصص (expertise) بسازد. این تمرکز ایده‌آل در اوایل کار است، زیرا توسعه‌دهندگان به دیدگاه بیشتر، دانش کاری و تجربه عملی نیاز دارند. گسترش بخش بالایی به طور اتفاقی بخش میانی را نیز گسترش می‌دهد؛ همانطور که توسعه‌دهندگان با فناوری‌های بیشتر و مصنوعات (artifacts) مرتبط روبرو می‌شوند، به ذخیره «چیزهایی که می‌دانید که نمی‌دانید» آن‌ها اضافه می‌شود.

![Figure2-4](Figure2-4.png)

در شکل ۲-۴، گسترش بالای هرم سودمند است زیرا برای تخصص (expertise) ارزش قائل می‌شوند. با این حال، «چیزهایی که می‌دانید» همچنین چیزهایی هستند که باید آن‌ها را به‌روز نگه دارید — هیچ چیز در دنیای نرم‌افزار ایستا (static) نیست. اگر یک توسعه‌دهنده در Ruby on Rails متخصص شود، اگر برای یک یا دو سال آن را نادیده بگیرد، آن تخصص دوام نخواهد داشت. چیزهایی که در بالای هرم قرار دارند برای حفظ تخصص نیازمند سرمایه‌گذاری زمانی هستند. در نهایت، اندازه بالای هرم یک فرد، عمق فنی (technical depth) اوست.

با این حال، با انتقال توسعه‌دهندگان به نقش معمار، ماهیت دانش تغییر می‌کند. بخش بزرگی از ارزش یک معمار، درک گسترده از فناوری و نحوه استفاده از آن برای حل مسائل خاص است. برای مثال، به عنوان یک معمار، دانستن اینکه پنج راه‌حل برای یک مسئله خاص وجود دارد، سودمندتر از داشتن تخصص (expertise) منحصر به فرد تنها در یکی از آن‌هاست. مهم‌ترین بخش‌های هرم برای معماران، بخش‌های بالایی و میانی هستند؛ اینکه بخش میانی تا چه حد به بخش پایینی نفوذ می‌کند، وسعت فنی (technical breadth) یک معمار را نشان می‌دهد، همانطور که در شکل ۲-۵ نشان داده شده است.

![Figure2-5](Figure2-5.png)

به عنوان یک معمار، وسعت (breadth) مهم‌تر از عمق (depth) است. از آنجایی که معماران باید تصمیماتی بگیرند که قابلیت‌ها را با محدودیت‌های فنی تطبیق دهد، درک گسترده از طیف وسیعی از راه‌حل‌ها ارزشمند است. بنابراین، برای یک معمار، اقدام عاقلانه این است که مقداری از تخصص به سختی به دست آمده را فدا کند و از آن زمان برای گسترش سبد (portfolio) خود استفاده کند، همانطور که در شکل ۲-۶ نشان داده شده است. همانطور که در نمودار به تصویر کشیده شده است، برخی از حوزه‌های تخصص باقی خواهند ماند، احتمالاً در حوزه‌های فناوری که به طور خاص لذت‌بخش هستند، در حالی که بقیه به طور مفیدی تحلیل می‌روند.

![Figure2-6](Figure2-6.png)

هرم دانش ما نشان می‌دهد که نقش معمار چقدر اساساً با نقش توسعه‌دهنده متفاوت است. توسعه‌دهندگان تمام دوران حرفه‌ای خود را صرف تقویت تخصص (expertise) می‌کنند و انتقال به نقش معمار به معنای تغییر در آن دیدگاه است، که بسیاری از افراد آن را دشوار می‌یابند. این به نوبه خود منجر به دو ناکارآمدی (dysfunctions) رایج می‌شود: اول، معماری که سعی می‌کند تخصص خود را در طیف وسیعی از حوزه‌ها حفظ کند، در هیچ‌کدام از آن‌ها موفق نمی‌شود و در این فرآیند خود را به شدت خسته می‌کند. دوم، این موضوع به صورت تخصص کهنه (stale expertise) خود را نشان می‌دهد — این حس اشتباه که اطلاعات قدیمی شما هنوز هم در لبه علم است. ما این را اغلب در شرکت‌های بزرگ می‌بینیم که در آن توسعه‌دهندگانی که شرکت را تأسیس کرده‌اند به نقش‌های رهبری رسیده‌اند اما هنوز تصمیمات فناوری را با استفاده از معیارهای باستانی می‌گیرند (به «ضدالگوی انسان غارنشین منجمد» («Frozen Caveman Anti-Pattern») در صفحه ۳۰ مراجعه کنید).

معماران باید بر وسعت فنی تمرکز کنند تا تیرهای بیشتری در ترکش خود برای پرتاب داشته باشند. توسعه‌دهندگانی که به نقش معمار منتقل می‌شوند ممکن است مجبور شوند روش نگرش خود به کسب دانش را تغییر دهند. متعادل کردن سبد (portfolio) دانش خود از نظر عمق در برابر وسعت، چیزی است که هر توسعه‌دهنده‌ای باید در طول دوران حرفه‌ای خود در نظر بگیرد.

----
Frozen Caveman Anti-Pattern

A behavioral anti-pattern commonly observed in the wild, the Frozen Caveman AntiPattern, describes an architect who always reverts back to their pet irrational concern for every architecture. For example, one of Neal’s colleagues worked on a system that featured a centralized architecture. Yet, each time they delivered the design to the client architects, the persistent question was “But what if we lose Italy?” Several years before, a freak communication problem had prevented headquarters from communicating with its stores in Italy, causing great inconvenience. While the chances of a reoccurrence were extremely small, the architects had become obsessed about this particular architectural characteristic.

Generally, this anti-pattern manifests in architects who have been burned in the past by a poor decision or unexpected occurrence, making them particularly cautious in the future. While risk assessment is important, it should be realistic as well. Understanding the difference between genuine versus perceived technical risk is part of the ongoing learning process for architects. Thinking like an architect requires overcoming these “frozen caveman” ideas and experiences, seeing other solutions, and asking more relevant questions.

----
## ضدالگوی انسان غارنشین منجمد (Frozen Caveman Anti-Pattern)

یک ضدالگوی رفتاری (behavioral anti-pattern) که به طور رایج در عمل مشاهده می‌شود، «ضدالگوی انسان غارنشین منجمد» (Frozen Caveman Anti-Pattern)، معماری را توصیف می‌کند که برای هر معماری، همیشه به دغدغه غیرمنطقی محبوب خود بازمی‌گردد. برای مثال، یکی از همکاران نیل بر روی سیستمی کار می‌کرد که دارای یک معماری متمرکز (centralized architecture) بود. با این حال، هر بار که آن‌ها طراحی را به معماران مشتری تحویل می‌دادند، سوال مداوم این بود: «اما اگر ایتالیا را از دست بدهیم چه؟» چندین سال قبل، یک مشکل ارتباطی نادر مانع از ارتباط دفتر مرکزی با فروشگاه‌هایش در ایتالیا شده بود و ناراحتی زیادی ایجاد کرده بود. در حالی که شانس تکرار مجدد آن بسیار کم بود، معماران در مورد این ویژگی معماری (architectural characteristic) خاص وسواس پیدا کرده بودند.

به طور کلی، این ضدالگو (anti-pattern) در معمارانی بروز می‌کند که در گذشته از یک تصمیم ضعیف یا رخداد غیرمنتظره آسیب دیده‌اند و این امر باعث می‌شود در آینده به طور خاص محتاط باشند. در حالی که ارزیابی ریسک (risk assessment) مهم است، باید واقع‌بینانه نیز باشد. درک تفاوت بین ریسک فنی واقعی (genuine technical risk) در مقابل ریسک فنی درک‌شده (perceived technical risk) بخشی از فرآیند یادگیری مداوم برای معماران است. فکر کردن مانند یک معمار نیازمند غلبه بر این ایده‌ها و تجربیات «انسان غارنشین منجمد»، دیدن راه‌حل‌های دیگر و پرسیدن سوالات مرتبط‌تر است.

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
## تحلیل بده‌بستان‌ها (Analyzing Trade-Offs)

فکر کردن مانند یک معمار تماماً درباره دیدن بده‌بستان‌ها (trade-offs) در هر راه‌حل، چه فنی و چه غیرفنی، و تحلیل آن بده‌بستان‌ها برای تعیین بهترین راه‌حل است. به نقل از مارک (یکی از نویسندگان شما):

> معماری آن چیزی است که نمی‌توانید در گوگل جستجو کنید.

همه چیز در معماری یک بده‌بستان (trade-off) است، به همین دلیل پاسخ مشهور به هر سوال معماری در جهان «بستگی دارد» است. در حالی که بسیاری از مردم به طور فزاینده‌ای از این پاسخ عصبانی می‌شوند، متاسفانه این حقیقت دارد. شما نمی‌توانید پاسخ این سوال را که آیا REST بهتر است یا پیام‌رسانی (messaging)، یا اینکه آیا میکروسرویس‌ها (microservices) سبک معماری (architecture style) درستی است، در گوگل جستجو کنید، زیرا واقعاً بستگی دارد. این به محیط استقرار (deployment environment)، محرک‌های تجاری (business drivers)، فرهنگ شرکت، بودجه‌ها، چارچوب‌های زمانی، مجموعه مهارت توسعه‌دهنده (developer skill set)، و ده‌ها عامل دیگر بستگی دارد. محیط، موقعیت و مسئله هر کسی متفاوت است، به همین دلیل معماری اینقدر سخت است. به نقل از نیل (یکی دیگر از نویسندگان شما):

> در معماری پاسخ درست یا غلطی وجود ندارد، فقط بده‌بستان‌ها (trade-offs) وجود دارند.

![Figure2-7](Figure2-7.png)

برای مثال، یک سیستم حراج کالا (item auction system) را در نظر بگیرید، همانطور که در شکل ۲-۷ نشان داده شده است، جایی که شخصی برای کالایی که برای حراج گذاشته شده است، پیشنهادی را ثبت می‌کند.

سرویس تولیدکننده پیشنهاد (Bid Producer service) یک پیشنهاد از طرف پیشنهاددهنده تولید می‌کند و سپس آن مبلغ پیشنهادی را به سرویس‌های ضبط پیشنهاد (Bid Capture)، ردیابی پیشنهاد (Bid Tracking) و تحلیل پیشنهاد (Bid Analytics) ارسال می‌کند. این کار می‌تواند با استفاده از صف‌ها (queues) به روش پیام‌رسانی نقطه به نقطه (point-to-point messaging) یا با استفاده از یک تاپیک (topic) به روش پیام‌رسانی انتشار-و-اشتراک (publish-and-subscribe messaging) انجام شود. معمار باید از کدام یک استفاده کند؟ شما نمی‌توانید پاسخ را در گوگل جستجو کنید. تفکر معماری نیازمند این است که معمار بده‌بستان‌های مرتبط با هر گزینه را تحلیل کرده و بهترین گزینه را با توجه به موقعیت خاص انتخاب کند.

![Figure2-8](Figure2-8.png)

![Figure2-9](Figure2-9.png)

دو گزینه پیام‌رسانی برای سیستم حراج کالا در شکل‌های ۲-۸ و ۲-۹ نشان داده شده‌اند، که شکل ۲-۸ استفاده از یک تاپیک (topic) در مدل پیام‌رسانی انتشار-و-اشتراک را نشان می‌دهد، و شکل ۲-۹ استفاده از صف‌ها (queues) در مدل پیام‌رسانی نقطه به نقطه را نشان می‌دهد.

مزیت آشکار (و راه‌حل به ظاهر بدیهی) برای این مسئله در شکل ۲-۸، توسعه‌پذیری معماری (architectural extensibility) است. سرویس تولیدکننده پیشنهاد فقط به یک اتصال به یک تاپیک (topic) نیاز دارد، برخلاف راه‌حل صف در شکل ۲-۹ که در آن تولیدکننده پیشنهاد باید به سه صف مختلف متصل شود. اگر سرویس جدیدی به نام تاریخچه پیشنهاد (Bid History) به دلیل نیاز به ارائه تاریخچه‌ای از تمام پیشنهادهای هر پیشنهاددهنده در هر حراج به این سیستم اضافه شود، هیچ تغییری در سیستم موجود لازم نخواهد بود. هنگامی که سرویس جدید تاریخچه پیشنهاد ایجاد می‌شود، می‌تواند به سادگی در تاپیکی که از قبل حاوی اطلاعات پیشنهاد است، مشترک شود. اما در گزینه صف که در شکل ۲-۹ نشان داده شده است، یک صف جدید برای سرویس تاریخچه پیشنهاد مورد نیاز خواهد بود و تولیدکننده پیشنهاد باید اصلاح شود تا یک اتصال اضافی به صف جدید اضافه کند. نکته اینجاست که استفاده از صف‌ها هنگام افزودن قابلیت پیشنهاد جدید، نیازمند تغییر قابل توجهی در سیستم است، در حالی که با رویکرد تاپیک هیچ تغییری در زیرساخت موجود لازم نیست. همچنین، توجه داشته باشید که تولیدکننده پیشنهاد در گزینه تاپیک بیشتر جداسازی شده (decoupled) است — تولیدکننده پیشنهاد نمی‌داند اطلاعات پیشنهاد چگونه یا توسط کدام سرویس‌ها استفاده خواهد شد. در گزینه صف، تولیدکننده پیشنهاد دقیقاً می‌داند که اطلاعات پیشنهاد چگونه (و توسط چه کسی) استفاده می‌شود، و از این رو بیشتر به سیستم همبسته (coupled) است.

با این تحلیل، به نظر می‌رسد که رویکرد تاپیک با استفاده از مدل پیام‌رسانی انتشار و اشتراک، انتخاب بدیهی و بهترین است. با این حال، به نقل از ریچ هیکی، خالق زبان برنامه‌نویسی Clojure:

> برنامه‌نویسان مزایای همه چیز و بده‌بستان‌های هیچ چیز را نمی‌دانند. معماران باید هر دو را درک کنند.

تفکر معماری یعنی نگاه کردن به مزایای یک راه‌حل معین، اما همچنین تحلیل جنبه‌های منفی یا بده‌بستان‌های (trade-offs) مرتبط با یک راه‌حل. با ادامه مثال سیستم حراج، یک معمار نرم‌افزار جنبه‌های منفی راه‌حل تاپیک را تحلیل می‌کند. در تحلیل تفاوت‌ها، ابتدا در شکل ۲-۸ توجه کنید که با یک تاپیک (topic)، هر کسی می‌تواند به داده‌های پیشنهاد دسترسی داشته باشد، که یک مسئله احتمالی در دسترسی به داده (data access) و امنیت داده (data security) را معرفی می‌کند. در مدل صف که در شکل ۲-۹ نشان داده شده است، داده‌های ارسال شده به صف فقط توسط مصرف‌کننده (consumer) خاصی که آن پیام را دریافت می‌کند قابل دسترسی است. اگر یک سرویس سرکش (rogue service) به یک صف گوش دهد، آن پیشنهادها توسط سرویس مربوطه دریافت نخواهند شد و بلافاصله یک اعلان درباره از دست رفتن داده (و در نتیجه یک رخنه امنیتی احتمالی) ارسال می‌شود. به عبارت دیگر، شنود کردن یک تاپیک (topic) بسیار آسان است، اما شنود یک صف (queue) اینطور نیست.

علاوه بر مسئله امنیتی، راه‌حل تاپیک در شکل ۲-۸ فقط از قراردادهای همگن (homogeneous contracts) پشتیبانی می‌کند. تمام سرویس‌هایی که داده‌های پیشنهاد را دریافت می‌کنند باید قرارداد (contract) و مجموعه داده‌های پیشنهاد یکسانی را بپذیرند. در گزینه صف در شکل ۲-۹، هر مصرف‌کننده (consumer) می‌تواند قرارداد خاص خود را متناسب با داده‌هایی که نیاز دارد، داشته باشد. برای مثال، فرض کنید سرویس جدید تاریخچه پیشنهاد به قیمت درخواستی فعلی به همراه پیشنهاد نیاز دارد، اما هیچ سرویس دیگری به آن اطلاعات نیاز ندارد. در این حالت، قرارداد باید اصلاح شود و تمام سرویس‌های دیگری که از آن داده استفاده می‌کنند را تحت تأثیر قرار دهد. در مدل صف، این یک کانال جداگانه خواهد بود، و در نتیجه یک قرارداد جداگانه که هیچ سرویس دیگری را تحت تأثیر قرار نمی‌دهد.

یک عیب دیگر مدل تاپیک که در شکل ۲-۸ نشان داده شده است این است که از نظارت بر تعداد پیام‌ها در تاپیک و در نتیجه قابلیت‌های مقیاس‌پذیری خودکار (auto-scaling) پشتیبانی نمی‌کند. با این حال، با گزینه صف در شکل ۲-۹، هر صف می‌تواند به طور جداگانه نظارت شود، و توازن بار (load balancing) برنامه‌ریزی‌شده برای هر مصرف‌کننده پیشنهاد اعمال شود تا هر کدام بتوانند به طور خودکار و مستقل از یکدیگر مقیاس‌پذیر شوند. توجه داشته باشید که این بده‌بستان (trade-off) به فناوری خاصی وابسته است، به این معنا که پروتکل پیشرفته صف‌بندی پیام (Advanced Message Queuing Protocol - AMQP) به دلیل جداسازی بین یک اکسچنج (exchange) (چیزی که تولیدکننده (producer) به آن ارسال می‌کند) و یک صف (queue) (چیزی که مصرف‌کننده (consumer) به آن گوش می‌دهد) می‌تواند از توازن بار و نظارت برنامه‌ریزی‌شده پشتیبانی کند.

با توجه به این تحلیل بده‌بستان، اکنون کدام گزینه بهتر است؟ و پاسخ؟ بستگی دارد! جدول ۲-۱ این بده‌بستان‌ها را خلاصه می‌کند.

نکته اینجاست که همه چیز در معماری نرم‌افزار یک بده‌بستان (trade-off) دارد: یک مزیت و یک عیب. فکر کردن مانند یک معمار یعنی تحلیل این بده‌بستان‌ها، و سپس پرسیدن «کدام یک مهم‌تر است: توسعه‌پذیری یا امنیت؟» تصمیم بین راه‌حل‌های مختلف همیشه به محرک‌های تجاری (business drivers)، محیط و مجموعه‌ای از عوامل دیگر بستگی خواهد داشت.

---
Understanding Business Drivers
Thinking like an architect is understanding the business drivers that are required for the success of the system and translating those requirements into architecture characteristics (such as scalability, performance, and availability). This is a challenging task that requires the architect to have some level of business domain knowledge and healthy, collaborative relationships with key business stakeholders. We’ve devoted several chapters in the book on this specific topic. In Chapter 4 we define various architecture characteristics. In Chapter 5 we describe ways to identify and qualify architecture characteristics. And in Chapter 6 we describe how to measure each of these characteristics to ensure the business needs of the system are met.

----
### درک محرک‌های تجاری

فکر کردن مانند یک معمار یعنی درک محرک‌های تجاری (business drivers) که برای موفقیت سیستم لازم هستند و ترجمه آن نیازمندی‌ها به ویژگی‌های معماری (architecture characteristics) (مانند مقیاس‌پذیری (scalability)، عملکرد (performance) و دسترس‌پذیری (availability)). این یک وظیفه چالش‌برانگیز است که نیازمند این است که معمار سطحی از دانش دامنه تجاری (business domain knowledge) و روابط سالم و مبتنی بر همکاری با ذی‌نفعان کلیدی تجاری (key business stakeholders) داشته باشد. ما چندین فصل از کتاب را به این موضوع خاص اختصاص داده‌ایم. در فصل ۴، ما ویژگی‌های معماری (architecture characteristics) مختلف را تعریف می‌کنیم. در فصل ۵، راه‌هایی برای شناسایی و تعیین کیفیت ویژگی‌های معماری را توصیف می‌کنیم. و در فصل ۶، ما چگونگی اندازه‌گیری هر یک از این ویژگی‌ها را توصیف می‌کنیم تا اطمینان حاصل شود که نیازهای تجاری سیستم برآورده می‌شوند.

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
## ایجاد تعادل بین معماری و کدنویسی عملی (Balancing Architecture and Hands-On Coding)

یکی از وظایف دشواری که یک معمار با آن روبرو می‌شود، چگونگی ایجاد تعادل بین کدنویسی عملی (hands-on coding) و معماری نرم‌افزار (software architecture) است. ما قویاً معتقدیم که هر معماری باید کدنویسی کند و بتواند سطح معینی از عمق فنی (technical depth) را حفظ کند (به «وسعت فنی» در صفحه ۲۵ مراجعه کنید). در حالی که این ممکن است یک کار آسان به نظر برسد، گاهی اوقات انجام آن بسیار دشوار است.

اولین نکته در تلاش برای ایجاد تعادل بین کدنویسی عملی و معمار نرم‌افزار بودن، اجتناب از تله گلوگاه (bottleneck trap) است. تله گلوگاه زمانی رخ می‌دهد که معمار مالکیت کدی را در مسیر بحرانی (critical path) یک پروژه (معمولاً کد چارچوب (framework code) زیربنایی) بر عهده گرفته و به یک گلوگاه برای تیم تبدیل می‌شود. این اتفاق می‌افتد زیرا معمار یک توسعه‌دهنده تمام‌وقت نیست و بنابراین باید بین ایفای نقش توسعه‌دهنده (نوشتن و تست کد منبع) و نقش معمار (ترسیم نمودارها، شرکت در جلسات، و خوب، شرکت در جلسات بیشتر) تعادل برقرار کند.

یک راه برای اجتناب از تله گلوگاه به عنوان یک معمار نرم‌افزار مؤثر، واگذاری مسیر بحرانی و کد چارچوب به دیگران در تیم توسعه و سپس تمرکز بر کدنویسی بخشی از قابلیت تجاری (business functionality) (یک سرویس یا یک صفحه) برای یک تا سه تکرار (iterations) آینده است. با انجام این کار سه اتفاق مثبت رخ می‌دهد. اول، معمار در حال کسب تجربه عملی در نوشتن کد محصول (production code) است در حالی که دیگر به یک گلوگاه در تیم تبدیل نمی‌شود. دوم، مسیر بحرانی و کد چارچوب به تیم توسعه (جایی که به آن تعلق دارد) توزیع می‌شود و به آن‌ها مالکیت و درک بهتری از بخش‌های سخت‌تر سیستم می‌دهد. سوم، و شاید مهم‌تر از همه، معمار همان کد منبع مرتبط با کسب‌وکار را می‌نویسد که تیم توسعه می‌نویسد و بنابراین بهتر می‌تواند با تیم توسعه از نظر رنجی که ممکن است با فرآیندها، رویه‌ها و محیط توسعه متحمل شوند، همذات‌پنداری کند.

با این حال، فرض کنید که معمار قادر به توسعه کد با تیم توسعه نیست. چگونه یک معمار نرم‌افزار می‌تواند همچنان عملی (hands-on) باقی بماند و سطحی از عمق فنی را حفظ کند؟ چهار راه اساسی وجود دارد که یک معمار می‌تواند همچنان در محل کار عملی باقی بماند بدون اینکه مجبور به «تمرین کدنویسی در خانه» باشد (اگرچه ما تمرین کدنویسی در خانه را نیز توصیه می‌کنیم).

راه اول انجام مکرر اثبات مفهوم (proof of concepts or POCs) است. این عمل نه تنها نیازمند این است که معمار کد منبع بنویسد، بلکه به اعتبارسنجی یک تصمیم معماری با در نظر گرفتن جزئیات پیاده‌سازی (implementation details) نیز کمک می‌کند. برای مثال، اگر یک معمار در تلاش برای تصمیم‌گیری بین دو راه‌حل کشینگ (caching) گیر کرده باشد، یک راه مؤثر برای کمک به این تصمیم‌گیری، توسعه یک مثال کاربردی در هر محصول کشینگ و مقایسه نتایج است. این به معمار اجازه می‌دهد تا از نزدیک جزئیات پیاده‌سازی و میزان تلاش مورد نیاز برای توسعه راه‌حل کامل را ببیند. همچنین به معمار اجازه می‌دهد تا ویژگی‌های معماری (architectural characteristics) مانند مقیاس‌پذیری (scalability)، عملکرد (performance) یا تحمل خطای (fault tolerance) کلی راه‌حل‌های مختلف کشینگ را بهتر مقایسه کند.

توصیه ما هنگام انجام کار اثبات مفهوم این است که، هر زمان که ممکن است، معمار باید بهترین کد با کیفیت محصول (production-quality code) را که می‌تواند، بنویسد. ما این عمل را به دو دلیل توصیه می‌کنیم. اول، اغلب اوقات، کد اثبات مفهوم یک‌بارمصرف وارد مخزن کد منبع (source code repository) می‌شود و به معماری مرجع (reference architecture) یا مثال راهنما برای دیگران تبدیل می‌شود. آخرین چیزی که یک معمار می‌خواهد این است که کد یک‌بارمصرف و نامرتب او نماینده کار معمولش باشد. دلیل دوم این است که با نوشتن کد اثبات مفهوم با کیفیت محصول، معمار تمرین نوشتن کد با کیفیت و خوش‌ساختار را به جای توسعه مداوم شیوه‌های بد کدنویسی، به دست می‌آورد.

راه دیگر برای اینکه یک معمار عملی باقی بماند این است که به برخی از داستان‌های بدهی فنی (technical debt stories) یا داستان‌های معماری (architecture stories) بپردازد و تیم توسعه را برای کار بر روی داستان‌های کاربری (user stories) عملکردی و حیاتی آزاد کند. این داستان‌ها معمولاً اولویت پایینی دارند، بنابراین اگر معمار فرصت تکمیل یک داستان بدهی فنی یا معماری را در یک تکرار (iteration) معین پیدا نکند، آخر دنیا نیست و به طور کلی بر موفقیت آن تکرار تأثیر نمی‌گذارد.

به طور مشابه، کار بر روی رفع اشکالات (bug fixes) در یک تکرار، راه دیگری برای حفظ کدنویسی عملی و در عین حال کمک به تیم توسعه است. در حالی که قطعاً جذاب نیست، این تکنیک به معمار اجازه می‌دهد تا تشخیص دهد که مسائل و ضعف‌ها ممکن است در کجای پایگاه کد (code base) و احتمالاً معماری وجود داشته باشند.

بهره‌گیری از اتوماسیون (automation) با ایجاد ابزارهای خط فرمان (command-line tools) و تحلیل‌گرهای (analyzers) ساده برای کمک به تیم توسعه در کارهای روزمره‌شان، راه عالی دیگری برای حفظ مهارت‌های کدنویسی عملی و در عین حال مؤثرتر کردن تیم توسعه است. به دنبال کارهای تکراری که تیم توسعه انجام می‌دهد بگردید و آن فرآیند را خودکار کنید. تیم توسعه برای این اتوماسیون سپاسگزار خواهد بود. برخی از نمونه‌ها عبارتند از اعتبارسنج‌های خودکار منبع برای کمک به بررسی استانداردهای کدنویسی خاصی که در سایر تست‌های لینت (lint tests) یافت نمی‌شوند، چک‌لیست‌های خودکار، و کارهای بازآرایی کد (code refactoring) دستی و تکراری.

اتوماسیون همچنین می‌تواند به شکل تحلیل معماری (architectural analysis) و توابع برازش (fitness functions) برای اطمینان از سرزندگی و انطباق (compliance) معماری باشد. برای مثال، یک معمار می‌تواند کد جاوا را در ArchUnit در پلتفرم جاوا بنویسد تا انطباق معماری را خودکار کند، یا توابع برازش سفارشی بنویسد تا ضمن کسب تجربه عملی، از انطباق معماری اطمینان حاصل کند. ما در فصل ۶ درباره این تکنیک‌ها صحبت می‌کنیم.

یک تکنیک نهایی برای عملی باقی ماندن به عنوان یک معمار، انجام مکرر بازبینی کد (code reviews) است. در حالی که معمار واقعاً کد نمی‌نویسد، حداقل درگیر کد منبع است. علاوه بر این، انجام بازبینی کد این مزیت افزوده را دارد که می‌توان از انطباق با تیم اطمینان حاصل کرد.