
# Entrust Project

## Entrust is 
* An **experience logging application** for health education learners
* An open source **knowledge base** for analysis of that experience
* A **dashboard** of experience progress
* Domain agnostic (designed to be extensible to any health field)
* Modular, blending existing knowledge structures and terminologies in a useful package

If you are a cyclist or runner, think of it as Strava or MapMyRun for doctors. 

## What does Entrust do?
Entrust tracks and analyzes experience. It creates a map for learners to navigate their educational terrain, using real information instead of intuition and guesswork. 
According to the [ACGME](http://www.acgme.org/), the education of physicians to practice independently is based on experience.  Medical school, residencies, and fellowships are ordered stretches of experience. The Entrust project aims to categorize and quantify experience.
1. Capture learner experience quickly and accurately through a highly intuitive **logging interface**
2. Query (ask questions about) and compute these experiences with a procedural **knowledge base** 
3. Capture **curriculum data** (rotations/ dates) so the level of each learner is known, and learners of similar levels can be compared with each other.
4. Use the resulting information to 
* Create experience dashboards that learners and teachers can use to identify learning gaps and make decisions about future learning.
* Inform the individual about their progress compared to others. Are you behind or ahead of the experience curve?
* Set learning goals, and provide clear custom visualizations of individual progress towards those goals.
* Award badges or micro credentials for goals obtained.
* Make certain that every individual (not just groups, means, or averages) in the school/ program is meeting their goals.
* With clear information about the experience of individuals, allow teachers to safely give the right level of supervision and independence.  

Entrust captures data about leaner experience, passes it through its knowledge of concepts like anatomy, disease, procedures, and delivers useful information about the learner's progress (over time, and compared to others) in clear dashboards that can be used to identify learning gaps or make informed decisions about what kinds of learning opportunities to pursue next (modify future behavior). 

## Entrustable Professional Activities ([EPA](https://www.aamc.org/download/379308/data/coreentrustableprofessionalactivities.pdf))
[Competency-based education](https://wire.ama-assn.org/education/taking-time-element-out-move-ume-gme?utm_source=49786&utm_medium=email&utm_content=https%3a%2f%2fwire.ama-assn.org%2feducation%2ftaking-time-element-out-move-ume-gme&utm_campaign=20180601+OHSU+Now) is dominating health education reform. Schools will need to know "What can this provider *do*?" as much as "What does this provider *know*?". Entrust exists to help answer that question. Traditionally, a framework of competencies and milestones are used to assess medical education but, as abstract concepts, they're difficult for both humans and computers to use. This is where EPAs come in. EPAs are observable units of core physician work like *doing a history and physical* or *placing an IV catheter*. As observable processes with discrete components, they are practical ways to assess what a doctor can "do" - and they are computable.  A learner is "entrustable" when they can do a task without direct supervision. 

*What happened with the learner cannot be inferred from what happened to the patient.* The only way for educators to get individual experiential information is for individual learners to enter it in an app - it can't be inferred from patient charts.

## Experience vs Knowledge
As far as they have value to patients, doctors offer two things:  Knowledge and wisdom.  Over time, only increasing experience builds expert judgment and expert technical skill. One can't learn to swim through lectures, reading, and memorization.

![alt text](https://i.imgur.com/DA5UcDe.jpg "Info vs Knowledge vs Wisdom")
Image:[@gapingvoid](https://informationversusknowledge-blog.tumblr.com/page/2)

Entrust aims to fill an information void in medical education: knowing what each*individual* learner has experienced. We know what classes and exams and scores each learner has had, but because of the randomness of human injury and disease, and the many different sites (clinics, hospitals) where learners might rotate, individual learners get highly variable experience. We can't assume all learners will get sufficient experience from their rotations, but we *need* all learners to get sufficient experience from their rotations.

## Logging Interface
The interface uses an intuitive partial text match of *natural clinical language* to capture the most accurate data in the fewest screen touches.  

![Imgur](https://i.imgur.com/D0vNpC6.png)

To make term searching as effortless as possible, we 
* avoid abstractions, like billing terms, that don't represent what the learner actually did or force the learner to search for alternative terms when the one they are looking for doesn't exist. 
* include each terms' known synonyms.

Importantly, each term is mapped to its most closely related [SNOMED](https://www.snomed.org/snomed-ct) or [CPT](https://www.ama-assn.org/practice-management/cpt-current-procedural-terminology) code (if it exists), to facilitate data analysis or import of old data. 

## Knowledge Base
The unique value of Entrust is that it can turn data (I did this surgery) into information (I experienced these things during that surgery) by using knowledge structures like ontologies and terminologies.  

This allows us to ask useful questions like *"How much experience does this learner have with injuries of the face?"* To a human, this is a simple question and can be answered by going through a user's experience line by line and asking "Is this finding an injury?" and "Is this anatomy part of the face?" For a computer, this requires the use of an ontology. An ontology is a set of concepts and categories in a subject area or domain that shows their properties and the relations between them.

In the example below, a learner logs a *Sagittal Ramus Osteotomy*. 

But because of the relations between that procedure and its known Processes (blue), Objects (tuquoise), and Anatomic Structures (green), we can infer all kinds of information from this one term. 

![Imgur](https://i.imgur.com/S74w1Iq.jpg)

Entrust will allow people with expert knowledge to create new and extended relational models like these (called graphs) from their domain of expertise into the novel graph database that powers the app. The more knowledge entered about what *is*, the more powerful our analysis of user experience.

## Dashboards

In order for information to be used by humans, it has to be concise and well formatted.  The human brain is able to quickly digest lines, colors, shapes, and sizes into information about the world.  Entrust has developed custom visualizations to represent experience, in many different and evolving formats, including anatomic heat maps.

![Imgur](https://i.imgur.com/U3n0Ui7.png?1)



## Getting Started/ Tools and Apps

Get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Neo4j Graph DB

Download neo4j community edition for graphDB visualization and editing. 

[neo4j Download](http://neo4j.com/download)

To run the current verion of the graph, copy the following directory to your local machine:

```
edexlog/tree/master/Neo4jGraphLocal/edex02_copy_localhost
```

Then point neo4j at your local directory, and his start.  It will run localhost/:7474

## ReadMe Authors

* Mark Engelstad - *Initial work* 

See also the list of [contributors](https://github.com/markengelstad/edexlog/graphs/contributors) who participate in this project.

## License

This project is licensed under the 

* Hat tip to anyone who's code was used
* Inspiration
* etc
