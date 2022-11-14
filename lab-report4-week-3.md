Lab 4 - Week 7

[Week 5 – Researching Commands](https://ucsd-cse15l-f22.github.io/week/week5/)

# grep -l
Is a command that lists all the names of the files that grep finds what its looking for in...

## Example 1: 
I put `$ grep -l "emergency" technical/*/*.txt` into to the command line for the example below:

```
[cs15lfa22ev@ieng6-201]:docsearch:37$ grep -l "emergency" technical/*/*.txt
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-3.txt
technical/911report/chapter-6.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/biomed/1471-2334-3-11.txt
technical/biomed/1471-2350-3-7.txt
technical/biomed/1471-2377-3-4.txt
technical/biomed/1471-2458-1-9.txt
technical/biomed/1471-2458-3-20.txt
technical/biomed/1472-684X-2-2.txt
technical/biomed/1472-6882-1-10.txt
technical/biomed/1472-6882-3-1.txt
technical/biomed/1472-6947-1-5.txt
technical/biomed/1472-6947-2-7.txt
technical/biomed/1472-6955-2-1.txt
technical/biomed/1472-6963-1-8.txt
technical/biomed/1472-6963-2-10.txt
technical/biomed/1472-6963-3-1.txt
technical/biomed/1472-6963-3-6.txt
technical/biomed/1472-6963-3-7.txt
technical/biomed/cc1044.txt
technical/biomed/cc1477.txt
technical/biomed/cc1497.txt
technical/biomed/cc1538.txt
technical/biomed/cc2171.txt
technical/biomed/cc300.txt
technical/biomed/cc303.txt
technical/biomed/cc713.txt
technical/biomed/cc973.txt
technical/biomed/cvm-2-1-038.txt
technical/biomed/cvm-2-6-286.txt
technical/biomed/rr37.txt
technical/plos/journal.pbio.0020121.txt
technical/plos/journal.pbio.0020263.txt
technical/plos/pmed.0020034.txt
technical/plos/pmed.0020059.txt
technical/plos/pmed.0020065.txt
technical/plos/pmed.0020140.txt
```
Above the command `$ grep -l "emergency" technical/*/*.txt` looked for the word "emergency" in the technical directory and it got the information of what files contained it. It printed out the name of many files and within all of them is the word emergency.

## Example 2:
I put `$ grep -l "maximiliano"  plos/*.txt` into to the command line for the example below:

```
[cs15lfa22ev@ieng6-201]:docsearch:44$ grep -l "maximiliano"  plos/*.txt
grep: plos/*.txt: No such file or directory
```
Above the command `$ grep -l "maximiliano"  plos/*.txt` looked for the word "max" in the  plos directory and it turns out that there is not occourance of that string within any of those files. So it returns a statement that says its not in there.

## Example 3:
I put `$ grep -l "emergency" plos/*.txt` into to the command line for the example below:

```
plos/journal.pbio.0020121.txt
plos/journal.pbio.0020263.txt
plos/pmed.0020034.txt
plos/pmed.0020059.txt
plos/pmed.0020065.txt
plos/pmed.0020140.txt
```

Above the command `$ grep -l "emergency" plos/*.txt` looked for the word "emergency" in the plos directory and it outputed the names of files that had the word we where looking for in it. This time there was words in the files that fit the description we where looking for and thats why it does not say no files match it this time.The command `grep -l` is useful to find the files that you are looking for an occurrence of a word. This is better then just using `grep` because without the `-l` it would print the files contents and it would give us a lot of text which would not be useful in helping us know what files contain the string occurrence.

# grep -c

Is a command that returns all the files we looked through, but it also tells us how many occurrences of the word we are looking for is in there...

## Example:
I put `$ grep -c "emergency" technical/*/*.txt` into to the command line for the example below:

```
...
technical/biomed/rr37.txt:4
technical/biomed/rr73.txt:0
technical/biomed/rr74.txt:0
...
technical/plos/journal.pbio.0020172.txt:0
technical/plos/journal.pbio.0020183.txt:0
technical/plos/journal.pbio.0020187.txt:0
technical/plos/journal.pbio.0020190.txt:0
technical/plos/journal.pbio.0020206.txt:0
technical/plos/journal.pbio.0020213.txt:0
technical/plos/journal.pbio.0020214.txt:0
technical/plos/journal.pbio.0020215.txt:0
technical/plos/journal.pbio.0020216.txt:0
technical/plos/journal.pbio.0020223.txt:0
technical/plos/journal.pbio.0020224.txt:0
technical/plos/journal.pbio.0020228.txt:0
technical/plos/journal.pbio.0020232.txt:0
technical/plos/journal.pbio.0020241.txt:0
technical/plos/journal.pbio.0020262.txt:0
technical/plos/journal.pbio.0020263.txt:1
technical/plos/journal.pbio.0020267.txt:0
technical/plos/journal.pbio.0020272.txt:0
technical/plos/journal.pbio.0020276.txt:0
technical/plos/journal.pbio.0020297.txt:0
technical/plos/journal.pbio.0020302.txt:0
technical/plos/journal.pbio.0020306.txt:0
technical/plos/journal.pbio.0020307.txt:0
technical/plos/journal.pbio.0020310.txt:0
technical/plos/journal.pbio.0020311.txt:0
technical/plos/journal.pbio.0020337.txt:0
technical/plos/journal.pbio.0020346.txt:0
technical/plos/journal.pbio.0020347.txt:0
technical/plos/journal.pbio.0020348.txt:0
technical/plos/journal.pbio.0020350.txt:0
technical/plos/journal.pbio.0020353.txt:0
technical/plos/journal.pbio.0020354.txt:0
technical/plos/journal.pbio.0020394.txt:0
technical/plos/journal.pbio.0020400.txt:0
technical/plos/journal.pbio.0020401.txt:0
technical/plos/journal.pbio.0020404.txt:0
technical/plos/journal.pbio.0020406.txt:0
technical/plos/journal.pbio.0020419.txt:0
technical/plos/journal.pbio.0020420.txt:0
technical/plos/journal.pbio.0020430.txt:0
technical/plos/journal.pbio.0020431.txt:0
technical/plos/journal.pbio.0020439.txt:0
technical/plos/journal.pbio.0020440.txt:0
technical/plos/journal.pbio.0030021.txt:0
technical/plos/journal.pbio.0030024.txt:0
technical/plos/journal.pbio.0030032.txt:0
technical/plos/journal.pbio.0030050.txt:0
technical/plos/journal.pbio.0030051.txt:0
technical/plos/journal.pbio.0030056.txt:0
technical/plos/journal.pbio.0030062.txt:0
technical/plos/journal.pbio.0030065.txt:0
technical/plos/journal.pbio.0030076.txt:0
technical/plos/journal.pbio.0030094.txt:0
technical/plos/journal.pbio.0030097.txt:0
technical/plos/journal.pbio.0030102.txt:0
technical/plos/journal.pbio.0030105.txt:0
technical/plos/journal.pbio.0030127.txt:0
technical/plos/journal.pbio.0030129.txt:0
technical/plos/journal.pbio.0030131.txt:0
technical/plos/journal.pbio.0030136.txt:0
technical/plos/journal.pbio.0030137.txt:0
technical/plos/pmed.0010008.txt:0
technical/plos/pmed.0010010.txt:0
technical/plos/pmed.0010013.txt:0
technical/plos/pmed.0010021.txt:0
technical/plos/pmed.0010022.txt:0
technical/plos/pmed.0010023.txt:0
technical/plos/pmed.0010024.txt:0
technical/plos/pmed.0010025.txt:0
technical/plos/pmed.0010026.txt:0
technical/plos/pmed.0010028.txt:0
technical/plos/pmed.0010029.txt:0
technical/plos/pmed.0010030.txt:0
technical/plos/pmed.0010034.txt:0
technical/plos/pmed.0010036.txt:0
technical/plos/pmed.0010039.txt:0
technical/plos/pmed.0010041.txt:0
technical/plos/pmed.0010042.txt:0
technical/plos/pmed.0010045.txt:0
technical/plos/pmed.0010046.txt:0
technical/plos/pmed.0010047.txt:0
technical/plos/pmed.0010048.txt:0
technical/plos/pmed.0010049.txt:0
technical/plos/pmed.0010050.txt:0
technical/plos/pmed.0010051.txt:0
technical/plos/pmed.0010052.txt:0
technical/plos/pmed.0010056.txt:0
technical/plos/pmed.0010058.txt:0
technical/plos/pmed.0010060.txt:0
technical/plos/pmed.0010061.txt:0
technical/plos/pmed.0010062.txt:0
technical/plos/pmed.0010064.txt:0
technical/plos/pmed.0010066.txt:0
technical/plos/pmed.0010067.txt:0
technical/plos/pmed.0010068.txt:0
technical/plos/pmed.0010069.txt:0
technical/plos/pmed.0010070.txt:0
technical/plos/pmed.0010071.txt:0
technical/plos/pmed.0020002.txt:0
technical/plos/pmed.0020005.txt:0
technical/plos/pmed.0020007.txt:0
technical/plos/pmed.0020009.txt:0
technical/plos/pmed.0020015.txt:0
technical/plos/pmed.0020016.txt:0
technical/plos/pmed.0020017.txt:0
technical/plos/pmed.0020018.txt:0
technical/plos/pmed.0020019.txt:0
technical/plos/pmed.0020020.txt:0
technical/plos/pmed.0020021.txt:0
technical/plos/pmed.0020022.txt:0
technical/plos/pmed.0020023.txt:0
technical/plos/pmed.0020024.txt:0
technical/plos/pmed.0020027.txt:0
technical/plos/pmed.0020028.txt:0
technical/plos/pmed.0020033.txt:0
technical/plos/pmed.0020034.txt:1
technical/plos/pmed.0020035.txt:0
technical/plos/pmed.0020036.txt:0
technical/plos/pmed.0020039.txt:0
technical/plos/pmed.0020040.txt:0
technical/plos/pmed.0020045.txt:0
technical/plos/pmed.0020047.txt:0
technical/plos/pmed.0020048.txt:0
technical/plos/pmed.0020050.txt:0
technical/plos/pmed.0020055.txt:0
technical/plos/pmed.0020059.txt:16
technical/plos/pmed.0020060.txt:0
technical/plos/pmed.0020061.txt:0
technical/plos/pmed.0020062.txt:0
technical/plos/pmed.0020065.txt:5
technical/plos/pmed.0020067.txt:0
technical/plos/pmed.0020068.txt:0
...
```

The usage of `grep -c` above is helpful to us because it alows us to go through all the files we want to and helps us get the info we want, but it tells us how many times this string appears in each file. The only bad part about this command is that there is a lot of files without it and they just get printed out as well which is ok, but it takes up a lot of space.


# grep -n

Is a command that returns the number of the line that the word can be found on for the file and if the word is not in the file then it will just output the file name with `:0` to say its on 0 lines.

## Example:
I put `$ grep -n  "emergency" technical/*/*.txt` into to the command line for the example below:

```
...
technical/plos/pmed.0020208.txt:0
technical/plos/pmed.0020209.txt:0
technical/plos/pmed.0020210.txt:0
technical/plos/pmed.0020212.txt:0
technical/plos/pmed.0020216.txt:0
technical/plos/pmed.0020226.txt:0
technical/plos/pmed.0020231.txt:0
technical/plos/pmed.0020232.txt:0
technical/plos/pmed.0020235.txt:0
technical/plos/pmed.0020236.txt:0
technical/plos/pmed.0020237.txt:0
technical/plos/pmed.0020238.txt:0
technical/plos/pmed.0020239.txt:0
technical/plos/pmed.0020242.txt:0
technical/plos/pmed.0020246.txt:0
technical/plos/pmed.0020247.txt:0
technical/plos/pmed.0020249.txt:0
technical/plos/pmed.0020257.txt:0
technical/plos/pmed.0020258.txt:0
technical/plos/pmed.0020268.txt:0
technical/plos/pmed.0020272.txt:0
technical/plos/pmed.0020273.txt:0
technical/plos/pmed.0020274.txt:0
technical/plos/pmed.0020275.txt:0
technical/plos/pmed.0020278.txt:0
technical/plos/pmed.0020281.txt:0
technical/911report/chapter-1.txt:74:    About five minutes after the hijacking began, Betty Ong contacted the American Airlines Southeastern Reservations Office in Cary, North Carolina, via an AT&T airphone to report an emergency aboard the flight. This was the first of several occasions on 9/11 when flight attendants took action outside the scope of their training, which emphasized that in a hijacking, they were to communicate with the cockpit crew. The emergency call lasted approximately 25 minutes, as Ong calmly and professionally relayed information about events taking place aboard the airplane to authorities on the ground.
technical/911report/chapter-1.txt:78:    At 8:21, one of the American employees receiving Ong's call in North Carolina, Nydia Gonzalez, alerted the American Airlines operations center in Fort Worth, Texas, reaching Craig Marquis, the manager on duty. Marquis soon realized this was an emergency and instructed the airline's dispatcher responsible for the flight to contact the cockpit. At 8:23, the dispatcher tried unsuccessfully to contact the aircraft. Six minutes later, the air traffic control specialist in American's operations center contacted the FAA's Boston Air Traffic Control Center about the flight. The center was already aware of the problem.
technical/911report/chapter-1.txt:88:    At 8:41, Sweeney told Woodward that passengers in coach were under the impression that there was a routine medical emergency in first class. Other flight attendants were busy at duties such as getting medical supplies while Ong and Sweeney were reporting the events.
technical/911report/chapter-1.txt:246:    If a hijack was confirmed, procedures called for the hijack coordinator on duty to contact the Pentagon's National Military Command Center (NMCC) and to ask for a military escort aircraft to follow the flight, report anything unusual, and aid search and rescue in the event of an emergency. The NMCC would then seek approval from the Office of the Secretary of Defense to provide military assistance. If approval was given, the orders would be transmitted down NORAD's chain of command.   
technical/911report/chapter-1.txt:266:FAA Awareness. Although the Boston Center air traffic controller realized at an early stage that there was something wrong with American 11, he did not immediately interpret the plane's failure to respond as a sign that it had been hijacked. At 8:14, when the flight failed to heed his instruction to climb to 35,000 feet, the controller repeatedly tried to raise the flight. He reached out to the pilot on the emergency frequency. Though there was no response, he kept trying to contact the aircraft.
technical/911report/chapter-1.txt:586:The Pentagon Teleconferences. Inside the National Military Command Center, the deputy director for operations immediately thought the second strike was a terrorist attack. The job of the NMCC in such an emergency is to gather the relevant parties and establish the chain of command between the National Command Authority-the president and the secretary of defense- and those who need to carry out their orders.
technical/911report/chapter-10.txt:47:            For the first time in history, all nonemergency civilian aircraft in the United
technical/911report/chapter-10.txt:77:                Organizing federal emergency assistance. One question was what kind of public
technical/911report/chapter-10.txt:91:                Reopening the financial markets. After extraordinary emergency efforts
technical/911report/chapter-12.txt:1412:                transportation and other parts of our critical infrastructure, organizing emergency
technical/911report/chapter-12.txt:1429:                    minimum infrastructure for emergency response. But federal homeland security
technical/911report/chapter-12.txt:1440:                government should require each state receiving federal emergency preparedness funds
technical/911report/chapter-12.txt:1454:            The attacks on 9/11 demonstrated that even the most robust emergency response
technical/911report/chapter-12.txt:1465:                    frameworks for emergency response. We strongly support the decision that federal
technical/911report/chapter-12.txt:1475:            Public safety organizations, chief administrative officers, state emergency
technical/911report/chapter-12.txt:1477:                regional focus within the emergency responder community and promote
technical/911report/chapter-12.txt:1508:                examined the emergency response to 9/11, witness after witness told us that despite
technical/911report/chapter-12.txt:1516:                stakeholders, to consider the need for standards for private sector emergency
technical/911report/chapter-12.txt:1522:                criteria and terminology for preparedness, disaster management, emergency
technical/911report/chapter-12.txt:1524:                in the World Trade Center emergency demonstrated the need for these standards.
technical/911report/chapter-13.2.txt:239:                interview (Nov. 19, 2003). On standard emergency training, see FAA report, "Air
technical/911report/chapter-13.2.txt:243:                urgency of the situation, he pushed an emergency button that simultaneously
technical/911report/chapter-13.2.txt:338:                SAMC notified United's headquarters of the emergency call from the flight attendant.
technical/911report/chapter-13.2.txt:1009:                emergency, see NMCC briefing (July 21, 2003).
technical/911report/chapter-13.3.txt:844:                "Miscellaneous Equipment" (emergency exit), 14 C.F.R.� 121.313 (2001); FAA
technical/911report/chapter-13.4.txt:66:                aircraft, which was forced to make an emergency landing in Okinawa. In 1996, Yousef
technical/911report/chapter-13.5.txt:1294:            18. For the NYPD supervising the emergency call system and employing more than 1,200
technical/911report/chapter-13.5.txt:1379:                7 (Mar. 22, 2004); Commission analysis of 911/PAPD calls. For some emergency
technical/911report/chapter-13.5.txt:1430:                scene, however, all decisions relating to evacuation or other emergency procedures
technical/911report/chapter-13.5.txt:1436:                announcements, as opposed to "emergency" announcements (such as to evacuate), was to
technical/911report/chapter-13.5.txt:2093:                command, control, and coordination during an emergency response. ICS provides a
technical/911report/chapter-13.5.txt:2387:            24. During the morning of September 11, the FAA suspended all nonemergency air
technical/911report/chapter-3.txt:638:                event of an emergency. Even so, rules implemented in the 1960s required air crews to
technical/911report/chapter-6.txt:742:                Afghanistan. Clarke's deputy, Roger Cressey, wrote to Berger that emergency CSG and
technical/911report/chapter-8.txt:139:                conducted an emergency security review, and the embassy in Yemen was closed. The CSG
technical/911report/chapter-8.txt:140:                had foreign emergency response teams, known as FESTs, ready to move on four hours'
technical/911report/chapter-9.txt:9:                local public servants, especially the first responders: fire, police, emergency
technical/911report/chapter-9.txt:54:                and exposed vulnerabilities in the World Trade Center's and the city's emergency
technical/911report/chapter-9.txt:58:                to ensure safety, and elevators stopped. The public-address system and emergency
technical/911report/chapter-9.txt:62:                Twin Towers. The 911 emergency call system was overwhelmed. The general evacuation
technical/911report/chapter-9.txt:87:            To manage fire emergency preparedness and operations, the Port Authority created the
technical/911report/chapter-9.txt:91:                with building occupants during an emergency.
technical/911report/chapter-9.txt:99:                use the emergency intercom phone to obtain specific information on how to proceed.
technical/911report/chapter-9.txt:109:                drill announcement advised participants that in the event of an actual emergency,
technical/911report/chapter-9.txt:112:                provided at the time of an emergency. Civilians were not informed that rooftop
technical/911report/chapter-9.txt:153:                emergency, a leading role would be played by the Special Operations Division. This
technical/911report/chapter-9.txt:165:                emergency call system. Its approximately 1,200 operators, radio dispatchers, and
technical/911report/chapter-9.txt:167:                of emergency response. When a 911 call concerned a fire, it was transferred to FDNY
technical/911report/chapter-9.txt:252:                response to the emergency," while the OEM was "designated the 'On Scene Interagency
technical/911report/chapter-9.txt:318:                many civilians may have been unable to use the emergency intercom phones, as they
technical/911report/chapter-9.txt:337:                emergency personnel to reach them. This advice was given to callers from the North
technical/911report/chapter-9.txt:419:                to remain in place, it did not correspond to any prewritten emergency
technical/911report/chapter-9.txt:575:            Around the city, the NYPD cleared major thoroughfares for emergency vehicles to
technical/911report/chapter-9.txt:1198:            The emergency response effort escalated with the crash of United 175 into the South
technical/911report/chapter-9.txt:1206:                emergency personnel inside, as well a number of individuals-both first responders
technical/911report/chapter-9.txt:1236:                stairs and observed that the power was lost and emergency lights activated.
technical/911report/chapter-9.txt:1468:                largest loss of life of any emergency response agency in history. The PAPD suffered
technical/911report/chapter-9.txt:1474:                moved quickly north and established an emergency operations command post at the
technical/911report/chapter-9.txt:1486:            The emergency response at the Pentagon represented a mix of local, state, and federal
technical/911report/chapter-9.txt:1489:                management structure for emergency response, was in place in the National Capital
technical/911report/chapter-9.txt:1499:                terrorist attack affected the daily operations and emergency management requirements
technical/911report/chapter-9.txt:1508:            While no emergency response is flawless, the response to the 9/11 terrorist attack on
technical/911report/chapter-9.txt:1510:                relationships and trust established among emergency responders; second, the adoption
technical/911report/chapter-9.txt:1562:                both sites will likely recur in any emergency of similar scale. The task looking
technical/911report/chapter-9.txt:1566:            Like the national defense effort described in chapter 1, the emergency response to
technical/911report/chapter-9.txt:1671:                911 operators and FDNY dispatch were not adequately integrated into the emergency
technical/911report/chapter-9.txt:1682:                disasters, it is important to integrate those taking 911 calls into the emergency
technical/911report/chapter-9.txt:1700:                would be "responsible for the management of the City's response to the emergency."
technical/911report/chapter-9.txt:1712:                by clearing emergency lanes to the WTC.
technical/911report/chapter-9.txt:1744:                emergency of this scale contributed to the early lack of units in the South Tower,
technical/911report/chapter-9.txt:1783:                not "responsible for the management of the City's response to the emergency," as the
technical/911report/chapter-9.txt:1825:            In May 2004, New York City adopted an emergency response plan that expressly
technical/biomed/1471-2334-3-11.txt:66:        A total of 296 patients were evaluated in the emergency
technical/biomed/1471-2334-3-11.txt:71:        discharged from the emergency room while 88 (30%) were
technical/biomed/1471-2334-3-11.txt:109:        emergency departments. Five patients (4%) visited the
technical/biomed/1471-2334-3-11.txt:219:        status on emergency room services revealed uninsured
technical/biomed/1471-2334-3-11.txt:220:        emergency patients were less likely to be admitted to the
technical/biomed/1471-2334-3-11.txt:221:        hospital than insured emergency patients. [ 19 ] Weissman
technical/biomed/1471-2350-3-7.txt:16:        contrast between the outcomes of elective versus emergency
technical/biomed/1471-2377-3-4.txt:375:            emergency medical service or in the emergency
technical/biomed/1471-2458-1-9.txt:74:        hospital emergency rooms in other practice settings. All
technical/biomed/1471-2458-1-9.txt:338:        another one. We believe the omission of emergency room
technical/biomed/1471-2458-1-9.txt:342:        emergency rooms is also of great value. We see the system
technical/biomed/1471-2458-1-9.txt:343:        described here as being complementary to emergency room
technical/biomed/1471-2458-1-9.txt:346:        earlier signal than will an emergency room based detection
technical/biomed/1471-2458-1-9.txt:348:        that don't warrant emergency room care.
technical/biomed/1471-2458-3-20.txt:9:        healthcare workers in emergency departments, intensive care
technical/biomed/1471-2458-3-20.txt:42:          The population of interest for the survey was emergency
technical/biomed/1472-684X-2-2.txt:454:        an emergency operation for intestinal obstruction in case
technical/biomed/1472-6882-1-10.txt:1500:        benefit as an emergency medicine for snake and scorpion
technical/biomed/1472-6882-3-1.txt:670:        emergency medicine, family medicine, sports medicine,
technical/biomed/1472-6947-1-5.txt:132:            rose), emergency room visits, psychological status, and
technical/biomed/1472-6947-1-5.txt:241:          patients entering an emergency department who were
technical/biomed/1472-6947-1-5.txt:244:          fellow-up care or return to the emergency room (ER),
technical/biomed/1472-6947-2-7.txt:420:          emergency rooms and hospitals will have detailed
technical/biomed/1472-6947-2-7.txt:483:          infarction, the time they are first seen by emergency
technical/biomed/1472-6947-2-7.txt:484:          technicians, the time they arrive at the emergency
technical/biomed/1472-6955-2-1.txt:15:          (HAZMAT) units, emergency, and law enforcement
technical/biomed/1472-6963-1-8.txt:154:          procedures, and emergency room visits were included.
technical/biomed/1472-6963-1-8.txt:242:          in the emergency room and 1% were diagnosed upon
technical/biomed/1472-6963-1-8.txt:275:          Four percent resulted in an emergency room visit and 20%
technical/biomed/1472-6963-2-10.txt:219:            and comorbidities, admission source, emergency or
technical/biomed/1472-6963-3-1.txt:19:          Congress did not rescind emergency Medicaid from illegal
technical/biomed/1472-6963-3-1.txt:52:          ineligible for nonemergency Medicaid for their first 5
technical/biomed/1472-6963-3-1.txt:65:          restricted to emergency Medicaid.
technical/biomed/1472-6963-3-1.txt:81:          restricted to emergency Medicaid) through SSI eligibility
technical/biomed/1472-6963-3-1.txt:148:        nonemergency Medicaid coverage using state-only funds.
technical/biomed/1472-6963-3-1.txt:364:        longer eligible for nonemergency Medicaid coverage. Using
technical/biomed/1472-6963-3-1.txt:368:        immigrants whose eligibility for nonemergency Medicaid
technical/biomed/1472-6963-3-1.txt:401:        the nonemergency care that hospitals provided (both as
technical/biomed/1472-6963-3-1.txt:403:        who lost nonemergency Medicaid eligibility due to the
technical/biomed/1472-6963-3-1.txt:415:        for services as emergency services that previously were
technical/biomed/1472-6963-3-1.txt:416:        categorized as nonemergency services in order to secure
technical/biomed/1472-6963-3-1.txt:418:        eligibility criteria for emergency and nonemergency
technical/biomed/1472-6963-3-6.txt:267:          0.001) and to have had an emergency room visit (25% vs.
technical/biomed/1472-6963-3-7.txt:128:          (e.g., pharmacy, laboratory), emergency room, operating
technical/biomed/1472-6963-3-7.txt:136:          use of resource intensive services such as the emergency
technical/biomed/1472-6963-3-7.txt:279:            hospitalized ($9,661); angina treated in emergency room
technical/biomed/1472-6963-3-7.txt:496:            level is an ambulatory care or emergency room
technical/biomed/cc1044.txt:56:        hospitalized for elective or emergency services, or whether
technical/biomed/cc1044.txt:104:        arrhythmias, heart failure, etc.), emergency admission
technical/biomed/cc1044.txt:137:        patients were admitted in an emergency state, the remaining
technical/biomed/cc1044.txt:175:        hypo/hyperglycemia, cardiac disease, emergency admission,
technical/biomed/cc1044.txt:222:        18.5% in emergency admissions, similar to Kishi's series
technical/biomed/cc1044.txt:223:        (16%) [ 29], but emergency admission was not considered a
technical/biomed/cc1477.txt:71:        admission was after emergency surgery, and the presence of
technical/biomed/cc1477.txt:139:          admission was more likely to be medical or emergency
technical/biomed/cc1497.txt:38:        the patient, and whether the surgery was emergency or
technical/biomed/cc1538.txt:18:        initial emergency life-saving surgery and prompt,
technical/biomed/cc1538.txt:436:          acute settings such as intensive care units, emergency
technical/biomed/cc1538.txt:443:          evaluation in an emergency room trauma bay. This might be
technical/biomed/cc1538.txt:453:          intra-hospital transport for emergency imaging (e.g.
technical/biomed/cc2171.txt:54:          addition, all patients who died in an emergency
technical/biomed/cc2171.txt:443:        crowding; for example, emergency rooms or ICUs might have
technical/biomed/cc300.txt:35:        bone mineral in emergency situations by means of
technical/biomed/cc303.txt:158:        complicated ventilation, admission source (home, emergency
technical/biomed/cc303.txt:265:          admitted from the emergency room, 73 (33%) from general
technical/biomed/cc303.txt:386:        In the rural centers, the emergency room (ER) was the
technical/biomed/cc713.txt:26:          emergency department he was hypotensive and had pain in
technical/biomed/cc973.txt:10:        units and emergency prehospital settings. The GCS provides
technical/biomed/cc973.txt:14:        as possible in emergency situations, and may be repeated at
technical/biomed/cc973.txt:131:        With the development of emergency medicine, a need arose
technical/biomed/cvm-2-1-038.txt:335:        well-coordinated center can perform emergency diffusion and
technical/biomed/cvm-2-1-038.txt:337:        duration comparable with that of emergency head CT. There
technical/biomed/cvm-2-6-286.txt:145:        including death, MI, emergency bypass surgery, and repeat
technical/biomed/rr37.txt:162:          subjects who appeared to rely on emergency department
technical/biomed/rr37.txt:270:          CI, 0-7%). Reliance on emergency department care was
technical/biomed/rr37.txt:353:        for asthma. Reliance on the emergency department for urgent
technical/biomed/rr37.txt:524:        reliance on emergency department for urgent asthma care,
technical/plos/journal.pbio.0020121.txt:40:        In 2001, the United States' Department of Agriculture (USDA) declared an emergency after
technical/plos/journal.pbio.0020263.txt:60:        nutritional deficits, exposure to pollutants, and the use of the emergency room as the sole
technical/plos/pmed.0020034.txt:92:        countries and to studies on acute asthma. In emergency room and hospital studies, the
technical/plos/pmed.0020059.txt:11:        of emergency department visits, primary care visits, ambulance dispatches, nurse hot line
technical/plos/pmed.0020059.txt:41:        relevant for surveillance data such as emergency department visits and pharmacy sales,
technical/plos/pmed.0020059.txt:47:        volume as the denominator. For example, one may use total emergency department visits as a
technical/plos/pmed.0020059.txt:63:        reports (for West Nile virus) [13], emergency department visits [7], ambulance dispatch
technical/plos/pmed.0020059.txt:66:        emergency department visits for diarrhea, respiratory, and fever/flu-like illnesses.
technical/plos/pmed.0020059.txt:74:          DOHMH seven days per week. Files contain data for all emergency department patient visits
technical/plos/pmed.0020059.txt:77:          illness. As of November 2002, 38 of New York City's 66 emergency departments were
technical/plos/pmed.0020059.txt:78:          participating in the system, covering an estimated 75% of emergency department visits in
technical/plos/pmed.0020059.txt:314:          emergency department data from 15 Nov 2001 to 14 Nov 2002, looking at diarrhea visits.
technical/plos/pmed.0020059.txt:363:          emergency department or coding differences between the emergency department triage
technical/plos/pmed.0020059.txt:387:        about the spatiotemporal characteristics of an outbreak. When using historical emergency
technical/plos/pmed.0020059.txt:441:        The emergency department data used in this study also have some limitations. In addition
technical/plos/pmed.0020059.txt:443:        reported to DOHMH during the historical 1-y period but not detected in emergency department
technical/plos/pmed.0020059.txt:445:        children that went to the emergency department of a nonparticipating hospital. Other
technical/plos/pmed.0020059.txt:446:        outbreaks went undetected because medical care was not sought in emergency departments.
technical/plos/pmed.0020059.txt:447:        Most people with diarrhea do not go to the hospital emergency department. Rather, they call
technical/plos/pmed.0020065.txt:12:        complaints of patients coming to the emergency room or calling a nurse hotline—are being
technical/plos/pmed.0020065.txt:19:        cases in every square kilometer), (ii) a control group (such as emergency visits not due to
technical/plos/pmed.0020065.txt:28:        applying it to data collected from hospital emergency departments in New York City. The
technical/plos/pmed.0020065.txt:37:        analyze emergency department data in New York City in parallel with other methods, and it
technical/plos/pmed.0020065.txt:43:        will be hard to cluster by place of residence or choice of emergency department.
technical/plos/pmed.0020140.txt:6:        An 18-year-old Caucasian male with type 1 diabetes presented to the emergency department
technical/plos/pmed.0020140.txt:154:          at some point during their lives [3]. Many of these patients undergo emergency surgery as
technical/plos/pmed.0020140.txt:157:          people with diabetes. The majority of patients with diabetes admitted for emergency
technical/plos/pmed.0020140.txt:162:          (Box 2), and frequently insulin requirement might increase during emergency surgery. It
technical/plos/pmed.0020140.txt:167:          emergency surgery procedures cannot be delayed, DKA can be treated concurrently with
technical/plos/pmed.0020140.txt:237:        Patients with type 1 diabetes undergoing elective or emergency surgical procedures have
```

Above I used `grep -n` and it went through the files we needed to look at and printed the line it can be found on and that specific line in the text, it also listed the files that did not contain it and put a 0 for the line number to say that it doesnt exist in the file. This is helpful for if you want to see where in the text you can find the word you are looking for because you get to know the line number and the words in the line.
