
### **Architecture Characteristics Defined****English Text:**
Architecture Characteristics Defined
A company decides to solve a particular problem using software, so it gathers a list of
requirements for that system. A wide variety of techniques exist for the exercise of
requirements gathering, generally defined by the software development process used
by the team. But the architect must consider many other factors in designing a soft‐
ware solution, as illustrated in Figure 4-1.
Figure 4-1. A software solution consists of both domain requirements and architecturalcharacteristics
Architects may collaborate on defining the domain or business requirements, but one
key responsibility entails defining, discovering, and otherwise analyzing all the things
the software must do that isn’t directly related to the domain functionality: architec‐
tural characteristics.
What distinguishes software architecture from coding and design? Many things,
including the role that architects have in defining architectural characteristics, the
important aspects of the system independent of the problem domain. Many organiza‐
tions describe these features of software with a variety of terms, including nonfunc‐
tional requirements, but we dislike that term because it is self-denigrating. Architects
created that term to distinguish architecture characteristics from functional require‐
ments, but naming something nonfunctional has a negative impact from a language
standpoint: how can teams be convinced to pay enough attention to something “non‐
functional”? Another popular term is quality attributes, which we dislike because it
implies after-the-fact quality assessment rather than design. We prefer architecture
characteristics because it describes concerns critical to the success of the architecture,
and therefore the system as a whole, without discounting its importance.
An architecture characteristic meets three criteria:
• Specifies a nondomain design consideration
• Influences some structural aspect of the design
• Is critical or important to application success
These interlocking parts of our definition are illustrated in Figure 4-2.
Figure 4-2. The differentiating features of architecture characteristics
The definition illustrated in Figure 4-2 consists of the three components listed, in
addition to a few modifiers:
Specifies a nondomain design consideration
When designing an application, the requirements specify what the application
should do; architecture characteristics specify operational and design criteria for
success, concerning how to implement the requirements and why certain choices
were made. For example, a common important architecture characteristic speci‐
fies a certain level of performance for the application, which often doesn’t appear
in a requirements document. Even more pertinent: no requirements document
states “prevent technical debt,” but it is a common design consideration for archi‐
tects and developers. We cover this distinction between explicit and implicit
characteristics in depth in “Extracting Architecture Characteristics from Domain
Concerns” on page 65.
56 | Chapter 4: Architecture Characteristics Defined
Influences some structural aspect of the design
The primary reason architects try to describe architecture characteristics on
projects concerns design considerations: does this architecture characteristic
require special structural consideration to succeed? For example, security is a
concern in virtually every project, and all systems must take a baseline of precau‐
tions during design and coding. However, it rises to the level of architecture char‐
acteristic when the architect needs to design something special. Consider two
cases surrounding payment in a example system:
Third-party payment processor
If an integration point handles payment details, then the architecture
shouldn’t require special structural considerations. The design should incor‐
porate standard security hygiene, such as encryption and hashing, but
doesn’t require special structure.
In-application payment processing
If the application under design must handle payment processing, the archi‐
tect may design a specific module, component, or service for that purpose to
isolate the critical security concerns structurally. Now, the architecture char‐
acteristic has an impact on both architecture and design.
Of course, even these two criteria aren’t sufficient in many cases to make this
determination: past security incidents, the nature of the integration with the third
party, and a host of other criteria may be present during this decision. Still, it
shows some of the considerations architects must make when determining how
to design for certain capabilities.
Critical or important to application success
Applications could support a huge number of architecture characteristics…but
shouldn’t. Support for each architecture characteristic adds complexity to the
design. Thus, a critical job for architects lies in choosing the fewest architecture
characteristics rather than the most possible.
We further subdivide architecture characteristics into implicit versus explicit archi‐
tecture characteristics. Implicit ones rarely appear in requirements, yet they’re neces‐
sary for project success. For example, availability, reliability, and security underpin
virtually all applications, yet they’re rarely specified in design documents. Architects
must use their knowledge of the problem domain to uncover these architecture char‐
acteristics during the analysis phase. For example, a high-frequency trading firm may
not have to specify low latency in every system, yet the architects in that problem
domain know how critical it is. Explicit architecture characteristics appear in require‐
ments documents or other specific instructions.In Figure 4-2, the choice of a triangle is intentional: each of the definition elements
supports the others, which in turn support the overall design of the system. The ful‐
crum created by the triangle illustrates the fact that these architecture characteristics
often interact with one another, leading to the pervasive use among architects of the
term trade-off.

----

**تعریف مشخصه‌های معماری**
شرکتی تصمیم می‌گیرد تا یک مسئله خاص را با استفاده از نرم‌افزار حل کند، بنابراین لیستی از نیازمندی‌ها را برای آن سیستم جمع‌آوری می‌کند. طیف گسترده‌ای از تکنیک‌ها برای تمرین جمع‌آوری نیازمندی‌ها وجود دارد که عموماً توسط فرآیند توسعه نرم‌افزاری که تیم استفاده می‌کند، تعریف می‌شوند. اما معمار باید عوامل بسیار دیگری را در طراحی یک راهکار نرم‌افزاری در نظر بگیرد، همانطور که در شکل ۴-۱ نشان داده شده است.
شکل ۴-۱. یک راهکار نرم‌افزاری شامل نیازمندی‌های دامنه و مشخصه‌های معماری است
معماران ممکن است در تعریف نیازمندی‌های دامنه یا کسب‌وکار همکاری کنند، اما یک مسئولیت کلیدی شامل تعریف، کشف و تحلیل تمام چیزهایی است که نرم‌افزار باید انجام دهد و مستقیماً به عملکرد دامنه مرتبط نیست: مشخصه‌های معماری (architectural characteristics).
چه چیزی معماری نرم‌افزار را از کدنویسی و طراحی متمایز می‌کند؟ موارد بسیاری، از جمله نقشی که معماران در تعریف مشخصه‌های معماری دارند، یعنی جنبه‌های مهم سیستم که مستقل از دامنه مسئله هستند. بسیاری از سازمان‌ها این ویژگی‌های نرم‌افزار را با اصطلاحات مختلفی توصیف می‌کنند، از جمله نیازمندی‌های غیرعملکردی (nonfunctional requirements)، اما ما این اصطلاح را نمی‌پسندیم زیرا خود-تخریب‌گر است. معماران این اصطلاح را برای تمایز مشخصه‌های معماری از نیازمندی‌های عملکردی ابداع کردند، اما نامیدن چیزی به عنوان غیرعملکردی از دیدگاه زبانی تأثیر منفی دارد: چگونه می‌توان تیم‌ها را متقاعد کرد که به چیزی «غیرعملکردی» توجه کافی داشته باشند؟ اصطلاح محبوب دیگر، صفات کیفیت (quality attributes) است که ما آن را نیز نمی‌پسندیم زیرا به جای طراحی، بر ارزیابی کیفیت پس از وقوع دلالت دارد. ما مشخصه‌های معماری (architecture characteristics) را ترجیح می‌دهیم زیرا دغدغه‌هایی را توصیف می‌کند که برای موفقیت معماری و در نتیجه کل سیستم حیاتی هستند، بدون آنکه از اهمیت آن بکاهد.
یک مشخصه معماری سه معیار را برآورده می‌کند:
*   یک ملاحظه طراحی غیرمرتبط با دامنه را مشخص می‌کند
*   بر جنبه‌ای ساختاری از طراحی تأثیر می‌گذارد*   برای موفقیت برنامه حیاتی یا مهم است
این بخش‌های درهم‌تنیده تعریف ما در شکل ۴-۲ نشان داده شده‌اند.
شکل ۴-۲. ویژگی‌های متمایزکننده مشخصه‌های معماری
تعریف نشان داده شده در شکل ۴-۲، علاوه بر چند اصلاح‌کننده، از سه جزء ذکر شده تشکیل شده است:
**یک ملاحظه طراحی غیرمرتبط با دامنه را مشخص می‌کند**
هنگام طراحی یک برنامه، نیازمندی‌ها مشخص می‌کنند که برنامه چه کاری باید انجام دهد؛ مشخصه‌های معماری، معیارهای عملیاتی و طراحی را برای موفقیت مشخص می‌کنند که به نحوه پیاده‌سازی نیازمندی‌ها و چرایی اتخاذ برخی تصمیمات مربوط می‌شود. به عنوان مثال، یک مشخصه معماری مهم و رایج، سطح معینی از کارایی (performance) را برای برنامه مشخص می‌کند که اغلب در سند نیازمندی‌ها ظاهر نمی‌شود. حتی مرتبط‌تر: هیچ سند نیازمندی بیان نمی‌کند که «از بدهی فنی (technical debt) جلوگیری کنید»، اما این یک ملاحظه طراحی رایج برای معماران و توسعه‌دهندگان است. ما این تمایز بین مشخصه‌های صریح (explicit) و ضمنی (implicit) را به تفصیل در بخش «استخراج مشخصه‌های معماری از دغدغه‌های دامنه» در صفحه ۶۵ پوشش می‌دهیم.
۵۶ | فصل ۴: تعریف مشخصه‌های معماری**بر جنبه‌ای ساختاری از طراحی تأثیر می‌گذارد**
دلیل اصلی که معماران سعی در توصیف مشخصه‌های معماری در پروژه‌ها دارند، به ملاحظات طراحی مربوط می‌شود: آیا این مشخصه معماری برای موفقیت به ملاحظات ساختاری خاصی نیاز دارد؟ به عنوان مثال، امنیت (security) تقریباً در هر پروژه‌ای یک دغدغه است و همه سیستم‌ها باید سطح پایه‌ای از اقدامات احتیاطی را در حین طراحی و کدنویسی در نظر بگیرند. با این حال، زمانی به سطح مشخصه معماری ارتقا می‌یابد که معمار نیاز به طراحی چیزی خاص داشته باشد. دو مورد پیرامون پرداخت را در یک سیستم نمونه در نظر بگیرید:
**پردازشگر پرداخت شخص ثالث**
اگر یک نقطه یکپارچه‌سازی (integration point) جزئیات پرداخت را مدیریت کند، معماری نباید به ملاحظات ساختاری خاصی نیاز داشته باشد. طراحی باید بهداشت امنیتی استاندارد مانند رمزگذاری (encryption) و هشینگ (hashing) را در بر گیرد، اما به ساختار خاصی نیاز ندارد.
**پردازش پرداخت درون‌برنامه‌ای**
اگر برنامه تحت طراحی باید پردازش پرداخت را انجام دهد، معمار ممکن است یک ماژول، مؤلفه یا سرویس خاص را برای آن منظور طراحی کند تا دغدغه‌های امنیتی حیاتی را به صورت ساختاری جدا کند. اکنون، مشخصه معماری هم بر معماری و هم بر طراحی تأثیر می‌گذارد.
البته، حتی این دو معیار نیز در بسیاری از موارد برای این تصمیم‌گیری کافی نیستند: حوادث امنیتی گذشته، ماهیت یکپارچه‌سازی با شخص ثالث و مجموعه‌ای از معیارهای دیگر ممکن است در طول این تصمیم‌گیری وجود داشته باشند. با این حال، این موارد برخی از ملاحظاتی را نشان می‌دهد که معماران باید هنگام تعیین نحوه طراحی برای قابلیت‌های خاص در نظر بگیرند.
**برای موفقیت برنامه حیاتی یا مهم است**
برنامه‌ها می‌توانند تعداد زیادی از مشخصه‌های معماری را پشتیبانی کنند... اما نباید این کار را بکنند. پشتیبانی از هر مشخصه معماری، پیچیدگی را به طراحی اضافه می‌کند. بنابراین، یک وظیفه حیاتی برای معماران، انتخاب کمترین تعداد مشخصه‌های معماری به جای بیشترین تعداد ممکن است.
ما مشخصه‌های معماری را به دو دسته مشخصه‌های معماری ضمنی (implicit) در مقابل صریح (explicit) تقسیم می‌کنیم. موارد ضمنی به ندرت در نیازمندی‌ها ظاهر می‌شوند، با این حال برای موفقیت پروژه ضروری هستند. به عنوان مثال، دسترس‌پذیری (availability)، پایایی (reliability) و امنیت (security) تقریباً زیربنای همه برنامه‌ها هستند، اما به ندرت در اسناد طراحی مشخص می‌شوند. معماران باید از دانش خود در مورد دامنه مسئله برای کشف این مشخصه‌های معماری در مرحله تحلیل استفاده کنند. به عنوان مثال، یک شرکت معاملات با فرکانس بالا ممکن است نیازی به مشخص کردن تأخیر کم (low latency) در هر سیستم نداشته باشد، اما معماران در آن دامنه مسئله می‌دانند که این موضوع چقدر حیاتی است. مشخصه‌های معماری صریح در اسناد نیازمندی‌ها یا سایر دستورالعمل‌های خاص ظاهر می‌شوند.
در شکل ۴-۲، انتخاب یک مثلث عمدی است: هر یک از عناصر تعریف، از دیگری پشتیبانی می‌کند و آن‌ها نیز به نوبه خود از طراحی کلی سیستم پشتیبانی می‌کنند. نقطه اتکایی که توسط مثلث ایجاد می‌شود، این واقعیت را نشان می‌دهد که این مشخصه‌های معماری اغلب با یکدیگر تعامل دارند و این امر منجر به استفاده فراگیر از اصطلاح موازنه (trade-off) در میان معماران می‌شود.

---

### **Architectural Characteristics (Partially) Listed**

Architecture characteristics exist along a broad spectrum of the software system,
ranging from low-level code characteristics, such as modularity, to sophisticated
operational concerns, such as scalability and elasticity. No true universal standard
exists despite attempts to codify ones in the past. Instead, each organization creates
its own interpretation of these terms. Additionally, because the software ecosystem
changes so fast, new concepts, terms, measures, and verifications constantly appear,
providing new opportunities for architecture characteristics definitions.
Despite the volume and scale, architects commonly separate architecture characteris‐
tics into broad categories. The following sections describe a few, along with some
examples.
Operational Architecture Characteristics
Operational architecture characteristics cover capabilities such as performance, scala‐
bility, elasticity, availability, and reliability. Table 4-1 lists some operational architec‐
ture characteristics.
Table 4-1. Common operational architecture characteristics
Term Definition
Availability How long the system will need to be available (if 24/7, steps need to be in place to allow the system to be
up and running quickly in case of any failure).
Continuity Disaster recovery capability.
Performance Includes stress testing, peak analysis, analysis of the frequency of functions used, capacity required, and
response times. Performance acceptance sometimes requires an exercise of its own, taking months to
complete.
Recoverability Business continuity requirements (e.g., in case of a disaster, how quickly is the system required to be online again?). This will affect the backup strategy and requirements for duplicated hardware.
Reliability/
safety
Assess if the system needs to be fail-safe, or if it is mission critical in a way that affects lives. If it fails, will
it cost the company large sums of money?
Robustness Ability to handle error and boundary conditions while running if the internet connection goes down or if
there’s a power outage or hardware failure.
Scalability Ability for the system to perform and operate as the number of users or requests increases.
Operational architecture characteristics heavily overlap with operations and DevOps
concerns, forming the intersection of those concerns in many software projects.
58 | Chapter 4: Architecture Characteristics Defined
Structural Architecture CharacteristicsArchitects must concern themselves with code structure. In many cases, the architect
has sole or shared responsibility for code quality concerns, such as good modularity,
controlled coupling between components, readable code, and a host of other internal
quality assessments. Table 4-2 lists a few structural architecture characteristics.
Table 4-2. Structural architecture characteristicsTerm Definition
Configurability Ability for the end users to easily change aspects of the software’s configuration (through usable
interfaces).
Extensibility How important it is to plug new pieces of functionality in.
Installability Ease of system installation on all necessary platforms.
Leverageability/
reuse
Ability to leverage common components across multiple products.
Localization Support for multiple languages on entry/query screens in data fields; on reports, multibyte character
requirements and units of measure or currencies.
Maintainability How easy it is to apply changes and enhance the system?
Portability Does the system need to run on more than one platform? (For example, does the frontend need to run
against Oracle as well as SAP DB?
Supportability What level of technical support is needed by the application? What level of logging and other facilities
are required to debug errors in the system?
Upgradeability Ability to easily/quickly upgrade from a previous version of this application/solution to a newer version
on servers and clients.
Cross-Cutting Architecture Characteristics
While many architecture characteristics fall into easily recognizable categories, many
fall outside or defy categorization yet form important design constraints and consid‐
erations. Table 4-3 describes a few of these.
Table 4-3. Cross-cutting architecture characteristics
Term Definition
Accessibility Access to all your users, including those with disabilities like colorblindness or hearing loss.
Archivability Will the data need to be archived or deleted after a period of time? (For example, customer accounts are
to be deleted after three months or marked as obsolete and archived to a secondary database for future
access.)
Authentication Security requirements to ensure users are who they say they are.
Authorization Security requirements to ensure users can access only certain functions within the application (by use case,
subsystem, webpage, business rule, field level, etc.).
Legal What legislative constraints is the system operating in (data protection, Sarbanes Oxley, GDPR, etc.)? What
reservation rights does the company require? Any regulations regarding the way the application is to be
built or deployed?
Architectural Characteristics (Partially) Listed | 59
Term Definition
Privacy Ability to hide transactions from internal company employees (encrypted transactions so even DBAs and
network architects cannot see them).
Security Does the data need to be encrypted in the database? Encrypted for network communication between
internal systems? What type of authentication needs to be in place for remote user access?
Supportability What level of technical support is needed by the application? What level of logging and other facilities are
required to debug errors in the system?
Usability/
achievability
Level of training required for users to achieve their goals with the application/solution. Usability
requirements need to be treated as seriously as any other architectural issue.
Any list of architecture characteristics will necessarily be an incomplete list; any soft‐
ware may invent important architectural characteristics based on unique factors (see
“Italy-ility” on page 60 for an example).
Italy-ility
One of Neal’s colleagues recounts a story about the unique nature of architectural
characteristics. She worked for a client whose mandate required a centralized archi‐
tecture. Yet, for each proposed design, the first question from the client was “But what
happens if we lose Italy?” Years ago, because of a freak communication outage, the
head office had lost communication with the Italian branches, and it was organiza‐
tionally traumatic. Thus, a firm requirement of all future architectures insisted upon
what the team eventually called Italy-ility, which they all knew meant a unique combi‐
nation of availability, recoverability, and resilience.
Additionally, many of the preceding terms are imprecise and ambiguous, sometimes
because of subtle nuance or the lack of objective definitions. For example, interopera‐
bility and compatibility may appear equivalent, which will be true for some systems.
However, they differ because interoperability implies ease of integration with other
systems, which in turn implies published, documented APIs. Compatibility, on theother hand, is more concerned with industry and domain standards. Another exam‐
ple is learnability. One definition is how easy it is for users to learn to use the soft‐
ware, and another definition is the level at which the system can automatically learn
about its environment in order to become self-configuring or self-optimizing using
machine learning algorithms.
Many of the definitions overlap. For example, consider availability and reliability,
which seem to overlap in almost all cases. Yet consider the internet protocol UDP,
which underlies TCP. UDP is available over IP but not reliable: the packets may arrive
out of order, and the receiver may have to ask for missing packets again.
No complete list of standards exists. The International Organization for Standards
(ISO) publishes a list organized by capabilities, overlapping many of the ones we’ve
listed, but mainly establishing an incomplete category list. The following are some of
the ISO definitions:
Performance efficiency
Measure of the performance relative to the amount of resources used under
known conditions. This includes time behavior (measure of response, processing
times, and/or throughput rates), resource utilization (amounts and types of
resources used), and capacity (degree to which the maximum established limits
are exceeded).
Compatibility
Degree to which a product, system, or component can exchange information
with other products, systems, or components and/or perform its required func‐
tions while sharing the same hardware or software environment. It includes coex‐
istence (can perform its required functions efficiently while sharing a common
environment and resources with other products) and interoperability (degree to
which two or more systems can exchange and utilize information).
Usability
Users can use the system effectively, efficiently, and satisfactorily for its intended
purpose. It includes appropriateness recognizability (users can recognize whether
the software is appropriate for their needs), learnability (how easy users can learn
how to use the software), user error protection (protection against users making
errors), and accessibility (make the software available to people with the widest
range of characteristics and capabilities).
Reliability
Degree to which a system functions under specified conditions for a specified
period of time. This characteristic includes subcategories such as maturity (does
the software meet the reliability needs under normal operation), availability
(software is operational and accessible), fault tolerance (does the software operate
as intended despite hardware or software faults), and recoverability (can the soft‐
ware recover from failure by recovering any affected data and reestablish the
desired state of the system.
Security
Degree the software protects information and data so that people or other prod‐
ucts or systems have the degree of data access appropriate to their types and lev‐
els of authorization. This family of characteristics includes confidentiality (data is
accessible only to those authorized to have access), integrity (the software pre‐
vents unauthorized access to or modification of software or data), nonrepudia‐
tion, (can actions or events be proven to have taken place), accountability (can
user actions of a user be traced), and authenticity (proving the identity of a user).
Architectural Characteristics (Partially) Listed | 61
Maintainability
Represents the degree of effectiveness and efficiency to which developers can
modify the software to improve it, correct it, or adapt it to changes in environ‐
ment and/or requirements. This characteristic includes modularity (degree to
which the software is composed of discrete components), reusability (degree to
which developers can use an asset in more than one system or in building other
assets), analyzability (how easily developers can gather concrete metrics about
the software), modifiability (degree to which developers can modify the software
without introducing defects or degrading existing product quality), and testability
(how easily developers and others can test the software).
Portability
Degree to which developers can transfer a system, product, or component from
one hardware, software, or other operational or usage environment to another.
This characteristic includes the subcharacteristics of adaptability (can developers
effectively and efficiently adapt the software for different or evolving hardware,
software, or other operational or usage environments), installability (can the soft‐
ware be installed and/or uninstalled in a specified environment), and replaceabil‐
ity (how easily developers can replace the functionality with other software).
The last item in the ISO list addresses the functional aspects of software, which we do
not believe belongs in this list:
Functional suitability
This characteristic represents the degree to which a product or system provides
functions that meet stated and implied needs when used under specified condi‐
tions. This characteristic is composed of the following subcharacteristics:
Functional completeness
Degree to which the set of functions covers all the specified tasks and user
objectives.
Functional correctness
Degree to which a product or system provides the correct results with the
needed degree of precision.
Functional appropriateness
Degree to which the functions facilitate the accomplishment of specified
tasks and objectives. These are not architecture characteristics but rather the
motivational requirements to build the software. This illustrates how think‐
ing about the relationship between architecture characteristics and the prob‐
lem domain has evolved. We cover this evolution in Chapter 7.

----

**فهرست (جزئی) مشخصه‌های معماری**
مشخصه‌های معماری در طیف وسیعی از سیستم نرم‌افزاری وجود دارند، از مشخصه‌های سطح پایین کد مانند ماژولار بودن (modularity) تا دغدغه‌های عملیاتی پیچیده مانند مقیاس‌پذیری (scalability) و کشسانی (elasticity). هیچ استاندارد جهانی واقعی وجود ندارد، علیرغم تلاش‌هایی که در گذشته برای تدوین آن‌ها صورت گرفته است. در عوض، هر سازمان تفسیر خود را از این اصطلاحات ایجاد می‌کند. علاوه بر این، از آنجا که اکوسیستم نرم‌افزار به سرعت تغییر می‌کند، مفاهیم، اصطلاحات، معیارها و روش‌های تأیید جدیدی به طور مداوم ظاهر می‌شوند که فرصت‌های جدیدی برای تعریف مشخصه‌های معماری فراهم می‌کنند.
علیرغم حجم و مقیاس، معماران معمولاً مشخصه‌های معماری را به دسته‌های گسترده‌ای تقسیم می‌کنند. بخش‌های زیر چند مورد را به همراه برخی مثال‌ها توصیف می‌کنند.
**مشخصه‌های معماری عملیاتی**
مشخصه‌های معماری عملیاتی قابلیت‌هایی مانند کارایی (performance)، مقیاس‌پذیری (scalability)، کشسانی (elasticity)، دسترس‌پذیری (availability) و پایایی (reliability) را پوشش می‌دهند. جدول ۴-۱ برخی از مشخصه‌های معماری عملیاتی را فهرست می‌کند.
جدول ۴-۱. مشخصه‌های معماری عملیاتی رایج

| اصطلاح                            | تعریف                                                        |
| :-------------------------------- | :----------------------------------------------------------- |
| دسترس‌پذیری (Availability)         | مدت زمانی که سیستم باید در دسترس باشد (اگر ۲۴/۷ باشد، باید اقداماتی برای راه‌اندازی سریع سیستم در صورت بروز هرگونه خرابی در نظر گرفته شود). |
| پیوستگی (Continuity)              | قابلیت بازیابی از فاجعه (Disaster recovery).                 |
| کارایی (Performance)              | شامل تست استرس (stress testing)، تحلیل پیک (peak analysis)، تحلیل فرکانس استفاده از توابع، ظرفیت مورد نیاز و زمان‌های پاسخ است. پذیرش کارایی گاهی به تمرین خاص خود نیاز دارد که ممکن است ماه‌ها طول بکشد. |
| بازیابی‌پذیری (Recoverability)     | نیازمندی‌های تداوم کسب‌وکار (به عنوان مثال، در صورت وقوع فاجعه، سیستم با چه سرعتی باید دوباره آنلاین شود؟). این موضوع بر استراتژی پشتیبان‌گیری و نیازمندی‌های سخت‌افزار تکراری تأثیر می‌گذارد. |
| پایایی/ایمنی (Reliability/safety) | ارزیابی اینکه آیا سیستم باید ضد-خطا (fail-safe) باشد، یا اینکه آیا به گونه‌ای مأموریت-بحرانی (mission-critical) است که بر زندگی افراد تأثیر بگذارد. اگر از کار بیفتد، آیا هزینه‌های هنگفتی برای شرکت به همراه خواهد داشت؟ |
| استواری (Robustness)              | توانایی مدیریت خطا و شرایط مرزی در حین اجرا در صورت قطع شدن اتصال اینترنت یا قطعی برق یا خرابی سخت‌افزار. |
| مقیاس‌پذیری (Scalability)          | توانایی سیستم برای اجرا و عملکرد با افزایش تعداد کاربران یا درخواست‌ها. |

----

### **The Many Ambiguities in Software Architecture**

A consistent frustration amongst architects is the lack of clear definitions of so many
critical things, including the activity of software architecture itself! This leads compa‐
nies to define their own terms for common things, which leads to industry-wide con‐
fusion because architects either use opaque terms or, worse yet, use the same terms
for wildly different meanings. As much as we’d like, we can’t impose a standard
nomenclature on the software development world. However, we do follow and rec‐
ommend the advice from domain-driven design to establish and use a ubiquitous lan‐
guage amongst fellow employees to help ensure fewer term-based misunderstandings.

----
**ابهامات فراوان در معماری نرم‌افزار**
یک ناامیدی مداوم در میان معماران، عدم وجود تعاریف واضح از بسیاری از موارد حیاتی است، از جمله خود فعالیت معماری نرم‌افزار! این امر باعث می‌شود شرکت‌ها اصطلاحات خود را برای موارد رایج تعریف کنند، که منجر به سردرگمی در سطح صنعت می‌شود زیرا معماران یا از اصطلاحات مبهم استفاده می‌کنند یا بدتر از آن، از اصطلاحات یکسان برای معانی کاملاً متفاوت استفاده می‌کنند. هر چقدر هم که بخواهیم، نمی‌توانیم یک نام‌گذاری استاندارد را بر دنیای توسعه نرم‌افزار تحمیل کنیم. با این حال، ما از توصیه طراحی دامنه-محور (domain-driven design) برای ایجاد و استفاده از یک زبان فراگیر (ubiquitous language) در میان همکاران پیروی و آن را توصیه می‌کنیم تا به اطمینان از سوء تفاهم‌های کمتر مبتنی بر اصطلاحات کمک کند.

---

### **Trade-Offs and Least Worst Architecture**
Applications can only support a few of the architecture characteristics we’ve listed for
a variety of reasons. First, each of the supported characteristics requires design effort
and perhaps structural support. Second, the bigger problem lies with the fact that
each architecture characteristic often has an impact on others. For example, if an
architect wants to improve security, it will almost certainly negatively impact perfor‐
mance: the application must do more on-the-fly encryption, indirection for secrets
hiding, and other activities that potentially degrade performance.A metaphor will help illustrate this interconnectivity. Apparently, pilots often struggle
learning to fly helicopters because it requires a control for each hand and each foot,
and changing one impacts the others. Thus, flying a helicopter is a balancing exercise,
which nicely describes the trade-off process when choosing architecture characteris‐
tics. Each architecture characteristic that an architect designs support for potentially
complicates the overall design.
Thus, architects rarely encounter the situation where they are able to design a system
and maximize every single architecture characteristic. More often, the decisions come
down to trade-offs between several competing concerns.
Never shoot for the best architecture, but rather the least worst
architecture.
Too many architecture characteristics leads to generic solutions that are trying to
solve every business problem, and those architectures rarely work because the design
becomes unwieldy.
This suggests that architects should strive to design architecture to be as iterative as
possible. If you can make changes to the architecture more easily, you can stress less
about discovering the exact correct thing in the first attempt. One of the most impor‐
tant lessons of Agile software development is the value of iteration; this holds true at
all levels of software development, including architecture.

_____
**موازنه‌ها و معماری با کمترین معایب**
برنامه‌ها به دلایل مختلف فقط می‌توانند از تعداد کمی از مشخصه‌های معماری که فهرست کرده‌ایم، پشتیبانی کنند. اول، هر یک از مشخصه‌های پشتیبانی شده نیاز به تلاش طراحی و شاید پشتیبانی ساختاری دارد. دوم، مشکل بزرگتر در این واقعیت نهفته است که هر مشخصه معماری اغلب بر دیگری تأثیر می‌گذارد. به عنوان مثال، اگر یک معمار بخواهد امنیت را بهبود بخشد، تقریباً به طور قطع بر کارایی (performance) تأثیر منفی خواهد گذاشت: برنامه باید رمزگذاری بیشتری را در لحظه (on-the-fly) انجام دهد، از غیرمستقیم‌سازی (indirection) برای پنهان کردن اسرار استفاده کند و فعالیت‌های دیگری که به طور بالقوه کارایی را کاهش می‌دهند.
یک استعاره به توضیح این ارتباط متقابل کمک می‌کند. ظاهراً، خلبانان اغلب برای یادگیری پرواز با هلیکوپتر دچار مشکل می‌شوند زیرا برای هر دست و هر پا به یک کنترل نیاز دارد و تغییر یکی بر دیگری تأثیر می‌گذارد. بنابراین، پرواز با هلیکوپتر یک تمرین تعادل است که به خوبی فرآیند موازنه (trade-off) را هنگام انتخاب مشخصه‌های معماری توصیف می‌کند. هر مشخصه معماری که یک معمار برای پشتیبانی از آن طراحی می‌کند، به طور بالقوه طراحی کلی را پیچیده می‌کند.
بنابراین، معماران به ندرت با وضعیتی مواجه می‌شوند که بتوانند سیستمی را طراحی کنند و تک تک مشخصه‌های معماری را به حداکثر برسانند. اغلب، تصمیمات به موازنه بین چندین دغدغه رقیب خلاصه می‌شود.
**هرگز به دنبال بهترین معماری نباشید، بلکه به دنبال معماری با کمترین معایب (least worst) باشید.**
وجود مشخصه‌های معماری بیش از حد، منجر به راهکارهای عمومی می‌شود که سعی در حل هر مشکل کسب‌وکاری دارند و این معماری‌ها به ندرت کار می‌کنند زیرا طراحی، سنگین و ناکارآمد می‌شود.
این نشان می‌دهد که معماران باید تلاش کنند تا معماری را تا حد امکان تکرارشونده (iterative) طراحی کنند. اگر بتوانید تغییرات را در معماری راحت‌تر اعمال کنید، می‌توانید استرس کمتری در مورد کشف چیز دقیقاً درست در اولین تلاش داشته باشید. یکی از مهم‌ترین درس‌های توسعه نرم‌افزار چابک (Agile)، ارزش تکرار است؛ این در تمام سطوح توسعه نرم‌افزار، از جمله معماری، صادق است.