# AppID-Magic
## Inspiration
Robert Lemm's brainchild

## What it does
This project was created to increase visibility into a network beyond the Palo Alto Networks provided AppID's, reduce the attack-surface and greatly reduce the amount of time it takes to research and create custom AppID's; most of which, would normally be a manual process.  Additionally, it also provides an easy way to write custom app-id's using machine-learning based on traffic patterns of unknown applications and querying threat logs for ssl & web-browsing traversing Palo Alto NGFW's.  All of the initial research has been automated and presented to XSOAR in the form of an incident.  Once the playbook associated with the incident is completed, the new custom AppID is then pushed to the NGFW/Panorama.  URL-Based AppID learning takes a threat log feed and displays the top-10 urls with ssl or web-browsing as the application and creates an incident with the relevant data to be selected and pushed to the NGFW or panorama.  The AppID engine to discover payloads/URL's was created with a previous project.  We used XSOAR to provide a mechanism to view the results from the discovery process and complete the process of creating custom AppID's on the NGFW/Panorama.

## How we built it
We used Python, Elastic Stack and unknown traffic logging to capture, cluster(machine-learning) and produce data to create an incident based on results from clustering.  In XSOAR, we created playbooks, automation, classifiers, layouts and custom fields to provide an easy workflow for completing the configuration process for the NGFW/Panorama.

## Challenges we ran into
Docker debates
Lots of discussions around the workflow process.
Debates around how to exchange/move data to XSOAR.


## Accomplishments that we're proud of
Everyone on the team contributed heavily to the process of getting results and formatting the data properly.  The most difficult task was interpreting XSOAR's context data to produce the correct XML structure for Firewall/Panorama commits.  We had to bring together a diverse team to learn from each others expertise.  Our team expertise consisted of automation, NGFW and security backgrounds.  No team member had all of these, which truly made it a team effort in formulating a solution.

## What we learned
A ton about XSOAR, but more importantly, howto automate workflows using incidents, playbooks, automation, classifiers and layouts.
## What's next for App-ID Magic
 -  Manual capture upload for analysis.
 - Add approval process to validate newly created Custom AppID.
 - Add reports for custom AppID's(number of appid's discovered/created etc....)
 - Data enrichment from incident and telemetry info.
 - Create packaging for back-end process(docker container) for ease of deployment.
