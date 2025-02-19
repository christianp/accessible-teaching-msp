# Accessibility project 2024

Made by Scarlett Spackman and Christian Lawson-Perfect as part of a
Summer project in 2024.

The purpose of this page is to show the importance of implementing
reasonable adjustments in response to student needs and to offer you
practical guidance on how to implement these adjustments efficiently. We
argue that adopting a more inclusive teaching style using universal
design principles is a good place to start and that embracing these
changes will foster a supportive and fair learning environment that
empowers each student, disabled or not, to reach their maximum
potential.

## More students are disclosing disabilities

There has been a 182% increase in the number of students declaring a
disability during their studies at Newcastle University over the past 9
years, rising from 1,458 in 2014/15 to 4,114 in 2023/24. In the same
period, the total student population has increased by only 25%. That is,
the proportion of students disclosing a disability has significantly
increased over the last decade. In 2014/15, only 6% of students
disclosed a disability, whereas in 2023/24, 14% of students did.

Focusing on more recent trends, there has been a notable increase in
disclosures of mental health disabilities in particular, from 587
students in 2018/19 to 1,281 students in 2023/24, a 118% increase.
Additionally, more students are disclosing multiple disabilities, with
the number rising from 182 in 2018/19 to 499 in 2023/24, a 174%
increase. This suggests an upward trend in the complexity of students'
access needs.

<!-- Charts -->
<div id="chartwrapper">
    <div id="disclosure_chart_2"></div>
    <div id="disclosure_chart_3"></div>
</div>

<!-- Highcharts JS -->
<script src="https://code.highcharts.com/highcharts.js" defer></script>
<script src="https://code.highcharts.com/modules/exporting.js" defer></script>
<script src="https://code.highcharts.com/modules/accessibility.js" defer></script>
<script src="https://code.highcharts.com/modules/series-label.js" defer></script>
<!-- Chart Scripts -->
<script>
    document.addEventListener("DOMContentLoaded", function () {
        Highcharts.chart("disclosure_chart_2", {
            chart: { type: "line" },
            title: { text: "Disability disclosure trends" },
            xAxis: {
                categories: [
                    "14/15",
                    "15/16",
                    "16/17",
                    "17/18",
                    "18/19",
                    "19/20",
                    "20/21",
                    "21/22",
                    "23/24",
                ],
                title: { text: "ACADEMIC YEAR" },
            },
            yAxis: {
                min: 1000,
                max: 4500,
                title: { text: "NUMBER OF STUDENTS" },
                labels: { format: "{value}" },
            },
            series: [
                {
                    name: "Students with disclosed disabilities",
                    data: [1458, 1919, 1956, 2017, 2597, 2298, 2740, 3484, 4114],
                    color: "#AD000C",
                    marker: { enabled: false },
                },
                {
                    name: "5% of student population",
                    data: [1156, 1190, 1249, 1324, 1361, 1404, 1389, 1364, 1440],
                    dashStyle: "ShortDot",
                    color: "black",
                    enableMouseTracking: false,
                    marker: { enabled: false },
                },
                {
                    name: "15% of student population",
                    data: [3467, 3569, 3747, 3971, 4082, 4211, 4166, 4092, 4319],
                    dashStyle: "ShortDot",
                    color: "black",
                    enableMouseTracking: false,
                    marker: { enabled: false },
                },
            ],
        });

        Highcharts.chart("disclosure_chart_3", {
            chart: { type: "line" },
            title: {
                text: "Mental health and multiple disability disclosures",
            },
            xAxis: {
                categories: [
                    "14/15",
                    "15/16",
                    "16/17",
                    "17/18",
                    "18/19",
                    "19/20",
                    "20/21",
                    "21/22",
                    "23/24",
                ],
                title: { text: "ACADEMIC YEAR" },
            },
            yAxis: {
                min: 0,
                max: 1500,
                title: { text: "NUMBER OF STUDENTS" },
                labels: { format: "{value}" },
            },
            series: [
                {
                    name: "Mental health difficulties",
                    data: [104, 248, 279, 322, 587, 461, 651, 1008, 1281],
                    color: "#007686",
                    marker: { enabled: false },
                },
                {
                    name: "Multiple disabilities",
                    data: [41, 81, 73, 72, 182, 126, 202, 330, 499],
                    color: "#a50088",
                    marker: { enabled: false },
                },
                {
                    name: "1% of student population",
                    data: [231, 238, 250, 265, 272, 281, 278, 273, 288],
                    dashStyle: "ShortDot",
                    color: "black",
                    enableMouseTracking: false,
                    marker: { enabled: false },
                },
            ],
        });
    });
</script>

In the MSP school 13% of the student population had an active SSP as of
2022/23. This is the highest proportion among all schools in SAgE, with
the School of Computing at 7%, the School of Engineering at 6%, and the
School of Natural and Environmental Sciences at 12%. Overall, SAgE had a
proportion of 9%.

However, even these figures do not tell the whole story. Disclosure
rates are generally low due to various factors, including stigma, lack
of enforcement of disability laws and guidelines, the fear of
discrimination, and the desire to assimilate with non-disabled peers
([Eccles et al., 2018; Ju et al., 2017; Mamboleo et al., 2019; Kohli
2018](#bibliography)). Indeed, research indicates that only about 35% of
students with disabilities disclose their disability to their university
([Newman & Madaus, 2015](#bibliography)). Within MSP then, using the
data from 2022/23, the proportion of students who are disabled or have a
diagnosed/diagnosable medical condition of some form could be as high as
37% (assuming that 35% of such students choose to disclose).

Indeed, in a 2022 survey by the mental health charity [Student
Minds](#bibliography), 57% of respondents self-reported a mental health
issue and 27% said they had a diagnosed mental health condition, the
official figure for students in the year 2021/22 was only 5% ([The
Higher Education Statistics Agency, 2023](#bibliography)).

These problems surrounding disclosure highlight that the university's
efforts to support disabled students need to address not only those who
disclose but also those who choose not to.

## Universal design for learning

[Universal Design for Learning
(UDL)](http://udloncampus.cast.org/home)
 is a proactive educational approach that
addresses diverse student needs by anticipating common access
requirements from the outset. It's much less effort for everyone
involved, students and instructors alike, when these needs are met
upfront.

With all of the modern educational tools we have at our disposal, the
possibilities for supporting students in their learning have widened
dramatically over the decades, but they are not being utilised.

Our lives are filled with technologies and tools that help people,
disabled or not, function more easily. Items like stairs, escalators,
scissors, washing machines, and other tools are accepted as essential
for any person's day-to-day functioning. No one questions their use or
considers them unnecessary accommodations. Yet, technologies and
supports designed to make life easier specifically for disabled
people---such as documents formatted in accessible ways---are often seen
as unnecessary, burdensome, or special treatment.

As [Wilson (2017)](#bibliography) notes, this disparity is an example of
what Alison Kafer calls the invisibility of nondisabled access and the
hypervisibility of disabled access. Both stairs and ramps provide
access, but only stairs go \"unmarked as access; indeed, it is only when
atypical bodies are taken into account that the question of access
becomes a problem.\" [(Kafer, 2013)](#bibliography).

UDL views disabled and non-disabled access needs at equal levels of
importance, utilising new tools and common adjustments to support all
students. Inclusive strategies ensure all students, whether disabled or
not, have equal access to learning. These adjustments, like providing
materials in advance or utilising lecture capture effectively, become
standard practices that benefit all learners. Embracing UDL is not a big
deal; it's simply about providing what each student needs to thrive and
making education fairer and more effective for all. Even small changes
can make a huge improvement in the educational outcomes and wellbeing of
students.

## Myths to bust

When it comes to accessible and inclusive teaching, several persistent
myths act as a barrier to the implementation of necessary accommodations
for students with disabilities. These myths reflect common
misconceptions and responses encountered when students request
reasonable adjustments.


### Students won't attend lectures if they are all on ReCap

Contrary to common concerns, there is no systematic evidence that
lecture capture leads to lower attendance! Although research on this
topic varies in conclusions and methodologies, a consistent finding
emerges: lecture capture has little to no impact on student attendance
nor academic achievement, and the benefits outweigh the potential
drawbacks.

Literature reviews by [Witthaus & Robinson (2015)](#bibliography) and
[Banerjee (2021)](#bibliography), support this conclusion. They
highlight that the real focus should be on maximizing the effectiveness
of lecture capture, rather than questioning its use. By emphasizing best
practices, we can transform lecture capture into a powerful educational
tool that enhances learning outcomes.

Moreover, the vast majority of students use lecture recordings as a
supplementary resource, not a replacement for in-person classes
[(Leadbeater et al., 2013)](#bibliography). This usage pattern
underscores the value of lecture capture in reinforcing and
complementing traditional learning.

To fully realize these benefits, it is suggested that lecturers should
clearly communicate the advantages and potential drawbacks of lecture
capture. Providing explicit guidance on how to effectively engage with
lecture recordings can help students avoid the potential negative
effects [(Leadbeater et al., 2013)](#bibliography).

### Disabled students' adjustments should be dealt with case-by-case

The current system of only providing adjustments to students on a
case-by-case basis using a Student Support Plan (SSP) is not fit for
purpose.

The increase in the number of students with disclosed disabilities at
Newcastle University indicates that we must consider a different
approach. The numbers speak for themselves: the number of students with
disclosed disabilities in 2010/11 was 1,075, the count has nearly
quadrupled to 4,114 in 2023/24, and more than doubled since 2017/18.

<div id="disclosure_chart"></div>

<script>
    document.addEventListener("DOMContentLoaded", function () {
        Highcharts.setOptions({
            colors: [
                "#04353e",
                "#ecbba2",
                "#00575b",
                "#5da505",
                "#ff939b",
            ],
        });

        Highcharts.chart("disclosure_chart", {
            chart: {
                type: "column",
            },
            title: {
                text: "Disclosed disabilities of students at Newcastle University from 2010 - 2023",
            },
            xAxis: {
                categories: [
                    "2010/11",
                    "2011/12",
                    "2012/13",
                    "2013/14",
                    "2014/15",
                    "2015/16",
                    "2016/17",
                    "2017/18",
                    "2018/19",
                    "2019/20",
                    "2020/21",
                    "2021/22",
                    "2022/23",
                    "2023/24",
                ],
            },
            yAxis: {
                labels: {
                    format: "{value}",
                },
                min: 0,
                title: {
                    text: null,
                },
            },
            tooltip: {
                pointFormat:
                    '<span style="color:{series.color}">{series.name}</span>: <b>{point.percentage:.2f}%</b><br/>',
                shared: true,
            },
            plotOptions: {
                column: {
                    stacking: "normal",
                },
            },
            series: [
                {
                    name: "Blind/partially sighted",
                    data: [
                        13, 12, 8, 15, 23, 24, 22, 24, 20, 21, 21, 22, 27, 34,
                    ],
                },
                {
                    name: "Wheelchair user/mobility difficulties",
                    data: [
                        21, 24, 31, 34, 36, 60, 49, 48, 47, 43, 48, 38, 40, 45,
                    ],
                },
                {
                    name: "Deaf/hearing impediment",
                    data: [
                        39, 42, 31, 30, 33, 40, 39, 45, 49, 46, 60, 65, 63, 73,
                    ],
                },
                {
                    name: "Autism spectrum condition",
                    data: [
                        12, 20, 37, 48, 48, 64, 73, 87, 130, 124, 146, 180, 214,
                        207,
                    ],
                },
                {
                    name: "Other/Disability not listed",
                    data: [
                        85, 105, 110, 124, 133, 177, 133, 154, 200, 160, 186,
                        197, 251, 172,
                    ],
                },
                {
                    name: "Unseen disability, e.g., diabetes, epilepsy",
                    data: [
                        119, 112, 112, 110, 129, 191, 214, 209, 267, 202, 257,
                        304, 336, 342,
                    ],
                },
                {
                    name: "Multiple disabilities",
                    data: [
                        15, 25, 24, 28, 41, 81, 73, 72, 182, 126, 202, 330, 381,
                        499,
                    ],
                },
                {
                    name: "Mental health difficulties",
                    data: [
                        56, 58, 69, 80, 104, 248, 279, 322, 587, 461, 651, 1008,
                        1193, 1281,
                    ],
                },
                {
                    name: "Learning difficulty e.g., Dyslexia",
                    data: [
                        715, 778, 774, 755, 911, 1034, 1074, 1056, 1115, 1115,
                        1169, 1340, 1432, 1461,
                    ],
                },
            ],
        });
    });
</script>

This explosive growth highlights a critical issue: the case-by-case
method is overwhelmed and unsustainable. Disabled students deserve a
system that proactively supports their needs rather than one that reacts
slowly and inconsistently. The current approach often leaves students
without essential adjustments, violating their rights under [The
Equality Act (2010)](#bibliography), causing unnecessary stress and
hindering their academic performance. It also places an unnecessary time
burden on module leaders through the expectation that they will read
through each SSP they are sent and implement each adjustment
individually.

There is a strong evidence base that implementing universal design for
learning (UDL) principles can address this problem effectively. UDL
emphasizes flexible learning environments that accommodate diverse
learning styles and needs from the outset, benefiting all students---not
just those with disabilities. By embedding accessibility into the very
fabric of educational practices, equitable access to learning
opportunities for everyone can be ensured.

Under a UDL framework, many common adjustments would be provided by
default, significantly reducing the workload associated with individual
SSPs. This proactive approach allows educators to focus their efforts on
more specific and uncommon adjustments that truly require individualized
attention. SSPs would still play a crucial role in addressing unique
needs, but their scope and complexity would be significantly
streamlined.

### Students will disclose their disability and have an appropriate SSP, or
will ask the module leader directly for adjustments

It is incorrect to assume that students will disclose their disability
to anybody at the university nor that they will subsequently receive an
appropriate SSP.

There are several reasons why a student may not disclose their
disability, including the fear of stigmatization, discrimination, or not
being taken seriously. In addition to this, some may not even know their
condition qualifies as a disability or may not have an accurate
diagnosis. This can leave students struggling without the support they
genuinely need which can affect their academic performance and
well-being. To highlight these points, consider the following quotes
from students at a UK university where [Eccles et al.
(2018)](#bibliography) conducted focus groups on the issue of disability
disclosure:

> "sometimes it's also about culture because in my country if you
> say you have a disability, you're just like pointed at, people
> point fingers at you, so you just prefer not to say or not be seen
> with a disability"

> "\[I\] didn't want to get diagnosed because I wanted to have the
> same opportunities as other students without disabilities"

> "I think if you have a mental disability, the stigma attached to
> that could potentially be that people will think you're not of
> sound mind, that you could be unpredictable, people usually expect
> the worst\..."

> "My flatmate's only just been diagnosed with anxiety, dyspraxia,
> dyscalculia and dyslexia, and only just now because she failed a
> unit\... so obviously she didn't fill it out on her form because
> she didn't know"

> "A lot of people are undiagnosed as well; like I've got slow
> processing, dyslexia, dyspraxia, and like - I just thought it was
> me, I thought it was normal"

> "They might just refuse to tell themselves that they're disabled
> in any way or not want to accept it"

> "I think it's quite non-specific so if somebody has something like
> maybe mental disability like anxiety or something like that, they
> wouldn't write it down because they don't think that they are
> properly disabled but they might technically be"

> "because it \[the application\] is so important, they wouldn't
> want to risk it - the risk associated with declaring a disability,
> the application could be rejected or turned down due to this
> factor"

Even when a student has disclosed their disability, the current system
is not especially effective for devising and implementing SSPs. It is
slow, bureaucratic, and not capable of giving students timely access to
the changes they need to make learning feasible. Additionally, there is
little to no guarantee that the alterations provided will be consistent.

Universal Design for Learning (UDL) is an effective solution to this
problem [(Schreuer & Sachs 2014)](#bibliography). UDL is an educational
framework based on the needs of various learners that is in place
beforehand, placing less importance on disclosures and SSPs.

Teaching under a UDL framework would a priori include some of the most
common adjustments required, such as providing lecture notes in advance
and creating course materials in an accessible format. This lessens the
need for individual disclosures and ensures that the students who do
require very specific individual adjustments can have them provided
efficiently. More tailor-made SSPs will still prove necessary for those
uncommon needs, but the system would be more efficient and not
scattergun, providing timelier and more focused support.

Furthermore, relying less on individual disclosure can lead to a more
inclusive and supportive campus culture. Students can be supported
without the worry of shame or the burden of proof that they are
\"disabled enough\" to need accommodations. This shift isn't only of
benefit to students with disabilities, but it improves the learning
environment for all.

A proactive, inclusive approach through UDL helps to ensure success for
each student and lessens the workload of module leaders. This shift to
inclusive teaching practices is urgently needed and has been advocated
for in the literature for a long time, yet evidence shows it is not
being done. To quote [Morina (2024)](#bibliography),

> "More than 20 years have passed since [Stage & Milne's study
> (1996)](#bibliography), yet the results are similar to those reported
> by the two most recent articles included in this systematic review
> [(Grimes et al. 2020; Vergunst & Swartz 2022)](#bibliography). This
> finding both surprises and concerns us, and prompts us to ask: have
> universities made so little progress over the years?".

### Adjustments provide an advantage to disabled students

The belief that adjustments provide an advantage to disabled students is
a common misconception. Reasonable adjustments are designed to level the
playing field, not to give any student an upper hand. They are essential
for ensuring equitable access to education, allowing all students to
demonstrate their abilities and knowledge under fair conditions.
[(Equality Act 2010, s.20)](#bibliography)

Reasonable adjustments, such as extended time for exams or alternative
assessment methods, are necessary to accommodate the diverse needs of
students with disabilities. These measures do not compromise academic
standards; instead, they uphold the integrity of the assessment process
by mitigating barriers that may otherwise impede the demonstration of a
disabled student's true capabilities. [(Equality and Human Rights
Commission, 2014)](#bibliography)

Indeed, [Vidal Rodeiro & Macinska (2022)](#bibliography) found that even
when accounting for group differences (e.g., socio-economic status) that
could affect performance, students who received accommodations for
high-stakes examinations (GCSE exams in the UK) performed similarly to
or slightly worse than students without accommodations. This highlights
that reasonable adjustments in fact equalize educational attainment and
opportunity across disabled and non-disabled students, rather than
providing an unfair advantage.

### Students learn more from handwritten notes

While some studies suggest that handwriting may enhance memory retention
for certain tasks, this perspective fails to consider the diverse needs
and abilities of all students, particularly those with disabilities.

Students with disabilities, such as dyslexia, dysgraphia, autism, ADHD,
and various physical impairments, can face significant challenges with
handwriting. For these students, the act of writing by hand can be a
barrier to effective learning. Dysgraphia, for instance, affects fine
motor skills and handwriting fluency, making it difficult for students
to take notes quickly and legibly. Similarly, students with dyslexia may
struggle with the speed and accuracy required for handwriting, while
those with ADHD or autism might find it hard to concentrate on both
listening and writing simultaneously.

Many students find it useful to engage with lecture material by
reviewing lecture notes prior to the class. By familiarizing themselves
with the content in advance, they can use the lecture to consolidate,
confirm, and expand their understanding ([Bui & Myerson,
2014](#bibliography)). This pre-lecture preparation can be particularly
beneficial for students who need more time to process information or who
benefit from a structured approach to learning and is especially useful
in complex and cognitively demanding subjects such as mathematics. Prior
access to materials containing lecture content can significantly enhance
comprehension and retention, particularly for students whose disability
may affect their processing speed and working memory.

Another important consideration is the use of \"gappy notes\", i.e.,
lecture notes that intentionally leave out proofs, examples, or key
details for students to fill in during the lecture. While this approach
might be intended to encourage active engagement, and some students find
them very useful, it can be particularly challenging for students with
disabilities if an alternative version with no gaps is not provided. For
example, students with processing difficulties or attention disorders
may struggle to fill in these gaps accurately and quickly, leading to
incomplete or incorrect notes.

## Things you can do

This section breaks down practical steps that you can take to integrate
accessibility into your module design and teaching. We explain why and
how to provide some common adjustments, which disabilities may
neccessitate such an adjustment and advice for when it may be difficult
to do this in practice.

### Providing all course materials in acccessible formats

#### Why should I do this?

Anybody can benefit from using assistive technology to aide their
studies. Assistive technology spans a broad range of tools which can be
anything from a screen reader to braille displays and screen magnifiers.
For a document to be accessible it must allow use of these assistive
technologies and be able to be adapted for specific needs.

#### How should I do this?

Creating accessible course materials involves following best practices
and using appropriate tools to ensure compatibility with assistive
technologies. Here are some detailed steps and recommendations:

##### Provide documents in accessible formats

###### HTML

What is considered an accessible document varies depending on the use,
but the "gold-standard" for accessible documents is HTML. PDFs can be
considered accessible in some ways, if they are created correctly, but
this is uncommon and time consuming. [Chirun is a tool which converts
LaTeX to an accessible HTML
format.](https://chirun.org.uk/)
 [Placeholder link for canvas
page]() 

###### Everything, everywhere

It's not just lecture notes that need to be accessible. Problem sheets,
solutions, statistical tables, slides, assignments, communications, etc.
all need to be available in an accessible format. There should not be
any course material without an accessible equivalent.

###### Canvas

Canvas is an accessible platform, anything posted on the Canvas course
(i.e., announcements, pages etc) is accessible for users of assistive
technology.

#### Design for Accessibility

##### Headings and structure

Use proper headings and a logical document structure. This helps screen
reader users navigate the document more easily.

##### Cognitive load

Consider how easy it is to find a specific resource and how easy they
are to use (i.e., if a problem sheet requires the use of a statistical
table include it on the problem sheet so students don't have to switch
between tabs/windows constantly).

##### Alt text

Provide descriptive alt text for all images, charts, and graphs to
convey the content to visually impaired users.

##### Tables

Ensure tables are used for data, not layout, and include proper headers
to make them accessible to screen readers.

##### Links

Use descriptive link text that makes sense out of context (e.g., "View
the syllabus" instead of "Click here").

##### Colours

Ensure sufficient color contrast between text and background to aid
readability for visually impaired users.

#### Who does it benefit?

Every student!

But in particular, the [Supportive Practice
Tool](https://www.ncl.ac.uk/learning-and-teaching/effective-practice/universal-design/supportive-practice-tool/)
 and the list of disability specific
[reasonable
adjustments](https://www.ncl.ac.uk/learning-and-teaching/support-and-student-skills/personal-tutoring/resources-and-training/reasonable-adjustments/)
 provided by Student Health and Wellbeing
Service (SHWS) suggest that the following disabilities/conditions may
necessitate this adjustment:

-   ADHD
-   Anxiety
-   Autism
-   Cancer
-   Chronic Fatigue Syndrome
-   D/deaf
-   Depression
-   Diabetes
-   Dyspraxia
-   Epilepsy
-   IBD and IBS
-   Migraine
-   Mobility difficulties
-   Specific Learning Difficulty (SpLD)
-   Visual Impairment

Note: this is not an all-encompassing nor exhaustive list. Some students
with the above disabilities/conditions may not require this adjustment
and many other disabilities/conditions not listed may necessitate this
adjustment

#### This might be difficult if [(need to fill text)]


### Consistently uploading materials in advance

#### Why should I do this?

Uploading course materials in advance provides substantial benefits for
students with disabilities, as well as the broader student population.
Neurodivergent students often experience difficulties with executive
functioning and working memory, which effects planning, organization,
and time management ([Christopher & Macdonald, 2005; Lukasik et al.,
2019; Habib et al., 2019; Barkley & Poillion, 1994](#bibliography)).

With advance access to lecture notes, students can preview the content
and organize their thoughts, allowing them to follow along more
effectively during lectures. This practice helps alleviate the cognitive
load that comes with simultaneously processing new information and
taking notes ([Bui and Myerson, 2014](#bibliography)).

In the context of subjects such as mathematics, physics, and statistics,
where lectures can be content-heavy and fast-paced, having access to
course materials beforehand allows students to familiarize themselves
with complex concepts and terminology. This pre-exposure can
significantly enhance their understanding and engagement during the
actual lecture.

In particular, autistic students often benefit from having predictable
and structured environments. Advance access to course materials helps
reduce anxiety and allows them to process information at their own pace,
leading to a more inclusive learning experience ([Gurbuz et al.,
2019](#bibliography)).

Students with physical disabilities, who may experience chronic pain or
fatigue, may face difficulties attending all classes or staying focused
throughout long lectures. These students may rely on pre-uploaded
materials to keep up with the coursework on days when their symptoms are
more severe.

By uploading materials in advance, you can help to ensure that students
are not disadvantaged by their disabilities and that all students can
engage with the course content in a flexible manner ([Sambrook & Rowley,
2010](#bibliography)).

#### How should I do this?

##### The basics

-   Ensure that materials are uploaded to Canvas at least one week in
    advance, the further in advance the better. This includes all course
    materials, i.e., lecture notes, slides, practice problems and
    solutions, etc.
-   All course materials being available on Canvas from the start of the
    semester is the ideal.
-   Materials being provided only 24 hours in advance should not be
    viewed as the standard, but as the bare minimum legal requirement.

##### Using a course schedule

Develop a course schedule outlining what will be covered, when it will
be covered, and when materials will be made available if they are not
already.

When creating this schedule, include enough detail so that, at the
beginning of the semester, students could feasibly search for and find
alternative external resources that are relevent to the course.

Ensure that this schedule is on the module's Canvas page at the point
of publication and stick to it as closely as possible. If changes must
be made to this schedule, communicate this to students as soon as
possible and update the relevant materials in a timely manner.

If it is truly not possible to provide a particular resource in advance,
provide students with outlines of key topics/theorems/results etc., so
that students are able to find alternative resources in advance of
teching sessions, and engourage them to do so. Perhaps also consider
collating some external resources to which you could point students to
in situations like this.

#### Who does it benefit?

Every student!

But in particular, the [Supportive Practice
Tool](https://www.ncl.ac.uk/learning-and-teaching/effective-practice/universal-design/supportive-practice-tool/)
 and the list of disability specific
[reasonable
adjustments](https://www.ncl.ac.uk/learning-and-teaching/support-and-student-skills/personal-tutoring/resources-and-training/reasonable-adjustments/)
 provided by Student Health and Wellbeing
Service (SHWS) suggest that the following disabilities/conditions may
necessitate this adjustment:

-   ADHD
-   Anxiety
-   Autism
-   Depression
-   Specific Learning Difficulty (SpLD)

Note: this is not an all-encompassing nor exhaustive list. Some students
with the above disabilities/conditions may not require this adjustment
and many other disabilities/conditions not listed may necessitate this
adjustment
:::

#### This might be difficult if [(need to fill text)]

* Your material is all handwritten.
* Your lecture delivery is highly interactive.
* It's all in slides.

### ReCap all in-person sessions 

#### Why should I do this?

Students with various mental disabilities, such as depression, anxiety,
specific learning disabilities (SpLD), ADHD, and autism, often
experience difficulties with working memory ( [Christopher and
Macdonald, 2005](#bibliography); [Lukasik et al., 2019](#bibliography);
[Grant, 2017](#bibliography); [Habib et al., 2019](#bibliography)). [Bui
and Myerson (2014)](#bibliography) note that in the context of lectures,
the task of note-taking directly correlates with part of the definition
of working memory: "the ability to temporarily store and manipulate
information." ( [Baddeley, 1992](#bibliography)). Students need to hold
the lecturer's words in their mind, understand and organize the
information, paraphrase it effectively, and write it down---all
simultaneously.

Additionally, students with physical disabilities may also struggle with
working memory due to their condition, often referred to as "brain fog"
([McWhirter et al., 2023](#bibliography)). For example, individuals with
chronic fatigue syndrome/myalgic encephalomyelitis (CFS/ME), long COVID,
fibromyalgia, and other conditions causing chronic pain and/or fatigue,
often experience working memory difficulties ( [Berryman et al.,
2013](#bibliography); [Callan et al., 2022](#bibliography); [Liu et al.,
2021](#bibliography)).

Providing access to high-quality lecture capture, along with guidance on
how to engage with this resource, is an effective way to support all
students' learning, particularly those with working memory challenges (
[Sanders, 2022](#bibliography); [Bennett, 2018](#bibliography)).

#### How should I do this?

It is important to recognise that in order to harness the benefits of
lecture capture, careful consideration must be taken in how the lecture
will be viewed as a recording.

That is, a ReCap recording of a black screen and audio of the lecture
(which may be difficult to hear if the instructor is not using a
microphone) will not provide the same benefits outlined above and does
not serve the intended purpose of lecture recording.

##### General guidance

-   Check that ReCap is set up and working correctly before every
    teaching session.
-   Ensure that anything that is visable or audible in the lecture is
    visable and audible in the ReCap recording.
-   Ensure you are using a microphone and that it works, even if you
    don't think it is needed.
-   If there are no lavalier/lapel microphones available in the teaching
    space, be mindful of where the ReCap audio is being recorded from
    and stay close to it and/or increase the volume of your speech.
-   Consider creating a backup plan for when the technology in the
    teaching space is not useable - there will always be the
    possiblility that the technology fails. This could include using
    your own devices to record the lecture live and uploading this to
    Canvas, or recording a new version of the lecture at a later time.

#### Who does it benefit?

Every student!

But in particular, the [Supportive Practice
Tool](https://www.ncl.ac.uk/learning-and-teaching/effective-practice/universal-design/supportive-practice-tool/)
 and the list of disability specific
[reasonable
adjustments](https://www.ncl.ac.uk/learning-and-teaching/support-and-student-skills/personal-tutoring/resources-and-training/reasonable-adjustments/)
 provided by Student Health and Wellbeing
Service (SHWS) suggest that the following disabilities/conditions may
necessitate this adjustment:

-   ADHD
-   Anxiety
-   Autism
-   Depression
-   Specific Learning Difficulty (SpLD)

Note: this is not an all-encompassing nor exhaustive list. Some students
with the above disabilities/conditions may not require this adjustment
and many other disabilities/conditions not listed may necessitate this
adjustment

#### This might be difficult if [(need to fill text)]

* Your preferred style of instruction is to use the boards
* Your lecture delivery is highly interactive.
* You do not feel confident with the technical skills required.

### Clear communication in writing 

#### Why should I do this?

Students with various mental disabilities, such as depression, anxiety,
specific learning disabilities (SpLD), ADHD, and autism often experience
difficulties with remembering verbal instructions and organizing
information ([Boucher, 2009](#bibliography); [Barkley,
2014](#bibliography); [Reid, 2016](#bibliography); [Christopher &
Macdonald, 2005](#bibliography); [Lukasik et al., 2019](#bibliography);
[Grant, 2017](#bibliography); [Habib et al., 2019](#bibliography)). For
example, autistic students may struggle to remember verbal instructions
and often prefer information in a visual format because it can be
processed and referred to over time, unlike spoken communication, which
is instant and quickly forgotten ( [Howard & Sedgewick,
2021](#bibliography)). Written communication allows students to refer
back to information as needed, reducing unnecassary cognitive load and
helping them stay organized.

Additionally, students with physical disabilities may also struggle with
cognitive functions due to their condition, often referred to as "brain
fog" ([McWhirter et al., 2023](#bibliography)). For example, individuals
with chronic fatigue syndrome/myalgic encephalomyelitis (CFS/ME), long
COVID, fibromyalgia, and other conditions causing chronic pain and/or
fatigue, often experience working memory difficulties ( [Berryman et
al., 2013](#bibliography); [Callan et al., 2022](#bibliography); [Liu et
al., 2021](#bibliography)). Clear written communication provides these
students with a reliable reference, reducing the need to rely on
impaired memory functions.

When written communication is not provided, students might spend
unnecessary time and effort re-watching lectures just to find specific
verbal statements/instructions, which can be particularly taxing for
those with limited time due to their disabilities ([Lambert & Dryer,
2017](#bibliography); [Holloway, 2001](#bibliography)), or they may miss
out on the information all together, putting them at a disadvantage.
Students with disabilities often face a higher cognitive load and
significant time constraints, indeed many disabled people describe
managing their disability as akin to having an additional job, involving
numerous administrative tasks and medical appointments ([Vickerman &
Blundell, 2010](#bibliography)). These responsibilities add to their
overall cognitive and time burdens. For these students, clear written
communication about key course information is not just a convenience but
a necessity.

This practice not only supports students with disabilities but also
improves the learning experience for all students by providing a
reliable reference that can be accessed at any time ( [Wilson,
2017](#bibliography); [Schelly et al., 2011](#bibliography)).

#### How should I do this?

##### The basics

###### Module changes

Communicate any changes to the structure or content of the module to
students **as soon as possible in as many forms as possible** . E.g., as
a Canvas announcement *and* as a lecture shout-out *and* mark any
revisions or updates on the relevent document and/or Canvas page.

###### Instructions

Where specific instructions are given to students, **provide a written
copy** . E.g., instructions on how to import a specific dataset/module
in R/Python, or when giving directions around campus.

###### Written summaries of verbal conversations

After one-on-one meetings or office hours, provide students with a
written summary of the key points discussed and any agreed-upon action
items or advice. Alternatively, allow (and engourage) the student to
make notes or record and be mindful of how fast you may be going, making
sure the student can keep up.

##### Canvas

###### Detailed syllabus/schedule

Provide a comprehensive syllabus and schedule on Canvas at the beginning
of the course that outlines the topics, *when* they will be covered, and
assignment deadlines.

###### Centralise key information

Ensure all key information is centralized in one easily accessible
location (i.e., the Modules page of your Canvas course). **Use clear
headings and subheadings** to organize content logically by date,
chapter or topic.

###### Mark duplicated resources, updates and revisions

If a particular resource is published on the Canvas course multiple
times (E.g., lecture notes in different formats, updated or redacted
versions of documents) **it should be clear to students where content is
duplicated, and where revisions or updates are made** (including
correction of typos) this should be noted so that students can
accuratley update their own notes.

##### Going the extra mile

The following suggestions are given to inspire you to consider different
ways you can communicate and present information to make your course
even more inclusive. Of course, they also provide more effective and
engaging education across the board!

###### Weekly outlines

Create weekly outlines that summarize the key concepts, objectives, and
tasks for each week. This helps students keep track of what they need to
focus on and prepare for, helping them manage their time effectively.

###### Summarise key definitions, theorems, etc

List and summarise key definitions, theorems, proofs, etc in a written
format to help students organise their revision. Tell students what must
be memorised and what will be provided in the exam.

###### FAQs

Maintain a frequently updated FAQ section on the course platform
addressing common questions from students and signposting additional
external resources or readings.

###### Student feedback

Regularly solicit feedback from students (in addition to the current
feedback mechanisms) about the clarity and accessibility of the written
materials, the Canvas course, and communication methods. Use this
feedback to make continuous improvements.

#### Who does it benefit?

Every student!

But in particular, the [Supportive Practice
Tool](https://www.ncl.ac.uk/learning-and-teaching/effective-practice/universal-design/supportive-practice-tool/)
 and the list of disability specific
[reasonable
adjustments](https://www.ncl.ac.uk/learning-and-teaching/support-and-student-skills/personal-tutoring/resources-and-training/reasonable-adjustments/)
 provided by Student Health and Wellbeing
Service (SHWS) suggest that the following disabilities/conditions may
necessitate this adjustment:

-   ADHD
-   Anxiety
-   Autism
-   Chronic Fatigue Syndrome
-   D/deaf
-   Depression
-   Diabetes
-   Dyspraxia
-   IBD and IBS
-   Migraine
-   Multiple Sclerosis (MS)
-   Specific Learning Difficulty (SpLD)
-   Visual Impairment

Note: this is not an all-encompassing nor exhaustive list. Some students
with the above disabilities/conditions may not require this adjustment
and many other disabilities/conditions not listed may necessitate this
adjustment

#### This might be difficult if [(need to fill text)]

* Your material is all handwritten.
* Your lecture delivery is highly interactive.
* It's all in slides.

## Bibliography

1.  [Baddeley, A. (1992). [Working
    memory.](https://doi.org/10.1126/science.1736359)
     Science, 255(5044), 556-559.]{#Baddeley}
2.  [Banerjee, S. (2021). [To capture the research landscape of lecture
    capture in university
    education.](https://doi.org/10.1016/j.compedu.2020.104032)
     Computers & education, 160,
    104032.]{#Banerjee}
3.  [Barkley, R. A., & Poillion, M. J. (1994). [Attention Deficit
    Hyperactivity Disorder: A Handbook for Diagnosis and
    Treatment.](https://doi.org/10.1177/019874299401900205)
     Behavioral Disorders, 19(2),
    150-152.]{#Barkley}
4.  [Bennett, W. J. (2018). [The use of lecture capture in the classroom
    environment](https://www.proquest.com/openview/a02853772d179f43d03dd5b0419110ce/1?pq-origsite=gscholar&cbl=18750)
     (Doctoral dissertation, Northcentral
    University).]{#Bennett}
5.  [Berryman, C., Stanton, T. R., Bowering, K. J., Tabor, A.,
    McFarlane, A., & Moseley, G. L. (2013). [Evidence for working memory
    deficits in chronic pain: a systematic review and
    meta-analysis.](https://journals.lww.com/pain/abstract/2013/08000/evidence_for_working_memory_deficits_in_chronic.6.aspx)
     Pain®, 154(8), 1181-1196.]{#Berryman}
6.  [Boucher, J. (2009). [The Autistic Spectrum: Characteristics, Causes
    and Practical
    Issues.](https://books.google.co.uk/books?id=XZVREAAAQBAJ)
     SAGE Publications.]{#Boucher}
7.  [Bui, D. C., & Myerson, J. (2014). [The role of working memory
    abilities in lecture
    note-taking.](https://doi.org/10.1016/j.lindif.2014.05.002)
     Learning and Individual Differences, 33,
    12-22.]{#Bui}
8.  [Callan, C., Ladds, E., Husain, L., Pattinson, K., & Greenhalgh, T.
    (2022). ['I can't cope with multiple inputs': a qualitative study of
    the lived experience of 'brain fog' after
    COVID-19.](https://bmjopen.bmj.com/content/12/2/e056366)
     BMJ open, 12(2), e056366.]{#Callan}
9.  [Christopher, G., & MacDonald, J. (2005). [The impact of clinical
    depression on working
    memory.](https://doi.org/10.1080/13546800444000128)
     Cognitive neuropsychiatry, 10(5),
    379-399.]{#Christopher}
10. [Eccles, S., Hutchings, M., Hunt, C., & Heaslip, V. (2018). [Risk
    and stigma: students' perceptions and disclosure of 'disability'
    in higher
    education.](https://doi.org/10.5456/WPLL.20.4.191)
     Widening Participation and Lifelong
    Learning, 20(4), 191-208.]{#Eccles}
11. [Elliott, C., & Neal, D. (2016). [Evaluating the use of lecture
    capture using a revealed preference
    approach.](https://doi.org/10.1177/1469787416637463)
     Active Learning in Higher Education,
    17(2), 153-167.]{#Elliott}
12. [[Equality Act 2010, c. 15, s. 20
    (UK).](https://www.legislation.gov.uk/ukpga/2010/15/section/20)
    ]{#EqualityAct}
13. [Equality and Human Rights Commission. (2014). [Equality Act 2010:
    Technical guidance on further and higher
    education.](https://www.equalityhumanrights.com/equality/equality-act-2010/technical-guidance-further-and-higher-education)
    ]{#EHRC}
14. [Grant, D. (2017). [That's the way I think: Dyslexia, dyspraxia,
    ADHD and dyscalculia
    explained.](https://psycnet.apa.org/doi/10.4324/9781315647005)
    ]{#Grant}
15. [Grimes, S., Southgate, E., Scevak, J., & Buchanan, R. (2020).
    [University student experiences of disability and the influence of
    stigma on institutional non-disclosure and
    Learning.](https://files.eric.ed.gov/fulltext/EJ1273678.pdf)
     Journal of Postsecondary Education and
    Disability, 33(1), 23-37.]{#Grimes}
16. [Gurbuz, E., Hanley, M. & Riby, D.M. (2019). [University Students
    with Autism: The Social and Academic Experiences of University in
    the UK.](https://doi.org/10.1007/s10803-018-3741-4)
     J Autism Dev Disord 49,
    617--631]{#Gurbuz}
17. [Habib, A., Harris, L., Pollick, F., & Melville, C. (2019). [A
    meta-analysis of working memory in individuals with autism spectrum
    disorders.](https://doi.org/10.1371/journal.pone.0216198)
     PloS one, 14(4), e0216198.]{#Habib}
18. [Higher Education Statistics Agency. (2023). [Higher education
    student statistics:
    2021/22.](https://www.hesa.ac.uk/news/19-01-2023/sb265-higher-education-student-statistics)
     (Accessed 13 September 2024).]{#HESA}
19. [Holloway, S. (2001). [The Experience of Higher Education from the
    Perspective of Disabled
    Students.](https://doi.org/10.1080/09687590120059568)
     Disability & Society, 16(4),
    597--615.]{#Holloway}
20. [Howard, P. L., & Sedgewick, F. (2021). ['Anything but the phone!':
    Communication mode preferences in the autism
    community.](https://doi.org/10.1177/13623613211014995)
     Autism, 25(8), 2265-2278.]{#Howard}
21. [Ju, S., Zeng, W., & Landmark, L. J. (2017). [Self-Determination and
    Academic Success of Students With Disabilities in Postsecondary
    Education: A
    Review.](https://doi.org/10.1177/1044207317739402)
     Journal of Disability Policy Studies,
    28(3), 180-189.]{#Ju}
22. [Kafer, A. (2013). [Feminist, Queer,
    Crip.](https://www.jstor.org/stable/j.ctt16gz79x)
     Indiana University Press.]{#Kafer}
23. [Kohli, J. (2018). [Exploring disability perspectives & perspective
    transformations among college
    students.](https://eric.ed.gov/?id=ED587974)
     (Doctoral dissertation, California State
    University, East Bay).]{#Kohli}
24. [Lambert, D. C., & Dryer, R. (2017). [Quality of Life of Higher
    Education Students with Learning Disability Studying
    Online.](https://doi.org/10.1080/1034912X.2017.1410876)
     International Journal of Disability,
    Development and Education, 65(4), 393--407.]{#Lambert}
25. [Leadbeater, W., Shuttleworth, T., Couperthwaite, J., &
    Nightingale, K. P. (2013). [Evaluating the use and impact of lecture
    recording in undergraduates: Evidence for distinct approaches by
    different groups of
    students.](https://doi.org/10.1016/j.compedu.2012.09.011)
     Computers & Education, 61,
    185-192.]{#Leadbeater}
26. [Liu, X., Yang, H., Li, S., Wan, D., Deng, Y., Fu, Y., \... & Hu, Y.
    (2021). [Mediating effects of working memory on the relationship
    between chronic pain and overgeneral autobiographical
    memory.](https://doi.org/10.1080/09658211.2021.1889606)
     Memory, 29(3), 298-304.]{#Liu}
27. [Lukasik, K. M., Waris, O., Soveri, A., Lehtonen, M., & Laine, M.
    (2019). [The relationship of anxiety and stress with working memory
    performance in a large non-depressed
    sample.](https://doi.org/10.3389/fpsyg.2019.00004)
     Frontiers in psychology, 10,
    417351.]{#Lukasik}
28. [Mamboleo, G., Dong, S., & Fais, C. (2020). [Factors Associated With
    Disability Self-Disclosure to Their Professors Among College
    Students With
    Disabilities.](https://doi.org/10.1177/2165143419893360)
     Career Development and Transition for
    Exceptional Individuals, 43(2), 78-88.]{#Mamboleo}
29. [McWhirter, L., Smyth, H., Hoeritzauer, I., Couturier, A., Stone,
    J., & Carson, A. J. (2023). [What is brain
    fog?.](https://jnnp.bmj.com/content/94/4/321)
     Journal of Neurology, Neurosurgery &
    Psychiatry, 94(4), 321-325.]{#McWhirter}
30. [Morina, A. (2024). [When what is unseen does not exist: disclosure,
    barriers and supports for students with invisible disabilities in
    higher
    education.](https://doi.org/10.1080/09687599.2022.2113038)
     Disability & Society, 39(4),
    914-932.]{#Morina}
31. [Newman, L. A., & Madaus, J. W. (2015). [Reported Accommodations and
    Supports Provided to Secondary and Postsecondary Students With
    Disabilities: National
    Perspective.](https://doi.org/10.1177/2165143413518235)
     Career Development and Transition for
    Exceptional Individuals, 38(3), 173-181.]{#Newman}
32. [Reid, G. (2016). [Dyslexia: A practitioner's
    handbook.](https://books.google.co.uk/books?id=iFWzCgAAQBAJ)
     John Wiley & Sons.]{#Reid}
33. [Sambrook, S., & Rowley, J. (2010). [What's the use of webnotes?
    Student and staff
    perceptions.](https://doi.org/10.1080/03098770903480338)
     Journal of Further and Higher Education,
    34(1), 119--134.]{#Sambrook}
34. [Sanders III, W. R. (2022). [The Effects of Lecture Capture Use and
    Student Engagement on the Exam Scores of First Year Pharmacy
    Students](https://www.proquest.com/openview/f46c5439073730be541a372f28835800/1?cbl=18750&diss=y&pq-origsite=gscholar)
     (Doctoral dissertation, The University of
    Alabama).]{#Sanders}
35. [Schelly, C. L., Davies, P. L., & Spooner, C. L. (2011). [Student
    perceptions of faculty implementation of Universal Design for
    Learning.](https://eric.ed.gov/?id=EJ941729)
     Journal of postsecondary education and
    disability, 24(1), 17-30.]{#Schelly}
36. [Schreuer, N., & Sachs, D. (2014). [Efficacy of accommodations for
    students with disabilities in higher
    education.](https://doi.org/10.3233/JVR-130665)
     Journal of Vocational Rehabilitation,
    40(1), 27-40.]{#Schreuer}
37. [Stage, F. K., & Milne, N. V. (1996). [Invisible Scholars: Students
    with Learning
    Disabilities.](https://doi.org/10.1080/00221546.1996.11780268)
     The Journal of Higher Education, 67(4),
    426--445.]{#Stage}
38. [Student Minds. (2023). [Insight Briefing February
    2023.](https://www.studentminds.org.uk/insight-briefings.html)
    ]{#StudentMinds}
39. [Vergunst, R., & Swartz, L. (2020). [Experiences with supervisors
    when students have a psychosocial disability in a university context
    in South
    Africa.](https://doi.org/10.1080/13562517.2020.1730784)
     Teaching in Higher Education, 27(5),
    695--708.]{#Vergunst}
40. [Vickerman, P., & Blundell, M. (2010). [Hearing the voices of
    disabled students in higher
    education.](https://doi.org/10.1080/09687590903363290)
     Disability & Society, 25(1),
    21--32.]{#Vickerman}
41. [Vidal Rodeiro, C., & Macinska, S. (2022) [Equal opportunity or
    unfair advantage? The impact of test accommodations on performance
    in high-stakes
    assessments.](https://doi.org/10.1080/0969594X.2022.2121680)
     Assessment in Education: Principles,
    Policy & Practice, 29(4), 462--481.]{#Vidal}
42. [Wilson, J. D. (2017). [Reimagining disability and inclusive
    education through universal design for
    learning.](https://dsq-sds.org/index.php/dsq/article/view/5417/4650)
     Disability Studies Quarterly,
    37(2).]{#Wilson}
43. [Witthaus, G. R., & Robinson, C. L. (2015). [Lecture capture
    literature review: A review of the literature from
    2012--2015.](https://repository.lboro.ac.uk/articles/online_resource/Lecture_capture_literature_review_A_review_of_the_literature_from_2012-2015/9368876)
     Loughborough: Centre for Academic
    Practice, Loughborough University.]{#Witthaus}

