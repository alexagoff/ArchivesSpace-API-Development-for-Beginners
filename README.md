# ArchivesSpace API Development for Beginners
This repository includes resources used for the mini-workshop “Have you tried the API?: ArchivesSpace API Development for Beginners” presented in May 2023 at the Northwest Archivists Annual Meeting.  

You'll find a small set of simple utility JSON scripts to be used with [Postman](https://www.postman.com/), a GUI for API development, in the subfolder [`Postman Collections`](Postman%20Collections). Combined with the live hands-on demonstration, these Postman Collections and support documentation should help users gain a basic understanding and use of the [ArchivesSpace API](https://archivesspace.github.io/archivesspace/api/) to extract data or make changes to their collection metadata at their home institutions. 

<br>

|Table of contents: |[Preparing for the workshop](#preparing-for-the-workshop)|[List of scripts](#list-of-scripts)|[Handouts](#handouts)|[Additional resources](#additional-resources)
|---|---|---|---|---|
<br>

## Preparing for the workshop
|[Download Participant Prep Guide PDF ⤵️](API%20Workshop%20-%20How%20to%20Prepare%20(Participants).pdf)|
|---|

<br>

## List of scripts 
Description of Postman Collection scripts in this repository:
- [`create_aspace_session.json`](/Postman%20Collections/create_aspace_session.json): Use to set a session with the ArchivesSpace API before using any other collections. Requires an environment variable for your institution's ArchivesSpace API (aspace_base_url) as well as user name (aspace_user) and password (aspace_password). Once a session is set, the ability to interact with ArchivesSpace records via the API will be based on permissions of the user account.
- [`update_accessions.json`](/Postman%20Collections/update_accessions.json): Appends something to the Content Description field in an Accession record. This collection does not overwrite the existing description field, new content is added to the end.
- [`update_agents.json`](/Postman%20Collections/update_agents.json): Changes the Source dropdown field in an Agent record.  Note that  to change the source, you must provide the Value from the Name Source (name_source) controlled value list, not the translation value that displays in the Agent record (ex. "lcnaf" instead of "Library of Congress Name Authority File).
- [`update_resources.json`](/Postman%20Collections/update_resources.json): Appends something to the repository processing note in an ArchivesSpace resource record.  This collection does not overwrite the existing content of the note.
- [`update_resources_note_field.json`](/Postman%20Collections/update_resources_note_field.json): Updates the Conditions Governing Access note(s) in a resource record if a specific string is present. Out of the box it is set up to look for the string "Reproduction and Permissions Request Form", but the user can change that to whatever. The collection uses a for loop to look through all notes attached to a resource record and an if statement to test whether the note is a Conditions Governing Access note.
- [`update_subjects.json`](/Postman%20Collections/update_subjects.json): Updates or adds a scope note to a subject record.  The uri for the subject record to be edited must be supplied. 

Empty template for Postman Environment for ArchivesSpace API: 
[`Empty ASpace Environment.postman_environment.json`](Empty%20ASpace%20Environment.postman_environment.json)

<br>

## Handouts 
Forthcoming
<!--
|[Download Cheatsheet PDF ⤵️](#)|
|---|

|[Download Slide Deck PDF ⤵️](#)|
|---|
-->
<br>

## Additional resources 
- [ArchivesSpace API Technical Documentation](https://archivesspace.github.io/archivesspace/api): Official docs for the ASpace API.
- [Postman Learning Center](https://learning.postman.com/): More learning material on API testing and development on the Postman platform.
- [Awesome ArchivesSpace](https://github.com/archivesspace/awesome-archivesspace): A wide-ranging list of web resources for ArchivesSpace users, including other scripts.
- [JSON](https://www.w3schools.com/js/js_json_intro.asp), [JavaScript](https://www.w3schools.com/js/), [Python](https://www.w3schools.com/python/default.asp): Suggested programming languages/syntax to aid in reading/writing basic utility scripts.
