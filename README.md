
# Entrust Project

## Entrust is 
1. An **experience logging application** for health education learners
2. An open source **knowledge base** for analysis of that experience
3. Domain agnostic (designed to be extensible to any health field)
4. Modular, blending existing knowledge structures and terminologies in a useful package

## What does Entrust do?
According to the [ACGME](http://www.acgme.org/), the education of physicians to practice independently is based on experience.  The Entrust project aims to 
1. Capture learner experience quickly and accurately through a highly intuitive **logging interface**
2. Query (ask questions about) and compute these experiences with a procedural **knowledge base** 
3. Capture **curriculum data** (rotations/ dates)
4. Use the resulting information to 
* Create experience dashboards that learners and teachers can use to identify learning gaps and where to concentrate future learning.
* Use data about the group to inform the individual about their progress. Are you behind or ahead of the experience curve?
* Provide clear custom visualizations of individual progress towards learning goals.
* Award badges or micro credentials for goals obtained.
* Make certain that every individual (not just groups) in the school/ program is meeting their goals.
* With clear information about the experience of individuals, allow teachers to safely give the right level of supervision and independence.  

Entrust captures data about leaner experience, passess it through its knowledge of anatomy and disease and procedures, and delivers useful information about the learner's progress (over time, and compared to others) in clear dashboards that can be used to find learning gaps or make informed decisions about what kinds of learning opportunities to pursue next. Its a map that lets learners navigate their educational terrain, using real information instead of intuition and guesswork. 

## Entrustable Professional Activities ([EPA](https://www.aamc.org/download/379308/data/coreentrustableprofessionalactivities.pdf))
Competency-based education is dominating health education reform. Schools need to know "What can this provider do?" as much as "What does this provider know?". Entrust exists to help answer that question. Traditionally, an elaborate framework of competencies and milestones are used to assess medical education but, as abstract concepts, they're difficult for both humans and computers to use. This is where EPAs come in. EPAs are observable units of core physican work like *doing a history and physical* or *placing an IV catheter*. As observable processes with discrete components, they are practical ways to assess what a doctor can "do" - and they are computable.  A learner is "entrustable" when they can do a task without direct supervision. The only way for educators to get individual experiential information is for individual learners to enter it in an app - it can't be inferred from patient charts.

## Experience vs Knowledge
As far as they have value to patients, doctors offer two things:  Knowledge and experience.  Over time, growth in experience is paramount because only increasing experience builds expert judgment and expert technical skill. One can't learn to swim through lectures, reading, and memorization.
![alt text](https://i.imgur.com/DA5UcDe.jpg "Info vs Knowledge vs Wisdom")
Image:[@gapingvoid](https://informationversusknowledge-blog.tumblr.com/page/2)

Entrust aims to fill an information void in medical education: knowing what each individual learner has experienced. We know what classes and exams and scores each learner has had, but because of the randomness of human injury and disease, and the many different sites (clinics, hospitals) where learners might rotate, individual learners get highly variable experience. We can't just assume that all learners will get sufficient experience. 

to revolutionize graduate medical surgical education through advanced informatics techniques including: semantically annotated user logs, graph databases, highly specific user feedback.  Revelog breaks learner experience into events with combinations of finding and procedures, each of which is analyzed for its nature/ action/ process as well as its site/ structure.  

## Logging Interface
![Imgur](https://i.imgur.com/D0vNpC6.png)
The interface uses an intuitive partial text match of *natural surgical language* to capture the most accurate data in the fewest screen touches.  We avoid using abstractions, like billing terms, that don't represent what the learner actually did, or force the learner to search for a second best term when the one they are looking for doesn't exist.  Lexical richness is enhanced by allowing the use of synonyms as well. 
## Knowledge Base
- a database of knowledge that allows the computer to "know" what a learner experienced during a reported event (which structures, objects, and processes, etc)
![Imgur](https://i.imgur.com/S74w1Iq.jpg)
![Imgur](https://i.imgur.com/U3n0Ui7.png?1)
## Dashboards


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
