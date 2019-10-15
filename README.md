# University of Liverpool's Autonomy and Verification Lab website
Matt Luckcuck 2019

## Contact and Theme

This website has been built by [Rafael Cardoso](https://rafaelcaue.github.io/) and [Matt Luckcuck](http://cgi.csc.liv.ac.uk/~mattlck/).

We are using the Jekyll theme [Slim Pickins](https://github.com/chrisanthropic/slim-pickins-jekyll-theme) as our base theme.

## Editing the Lab's Website

This website is built using [Jekyll](https://jekyllrb.com/), which compiles the files in this repository to produce a static HTML website.

The website can be edited either by cloning the repository and working locally, or directly in GitHub. Whichever method is used, _when you want to make your changes live_, make sure you **commit your changes to the master branch**. GitHub pages will automatically compile the files on the master branch, after a commit.

To reiterate this, **anything committed to the master branch will go live automatically**.

## Adding an Event Page

To add a new event page, make a new markdown file in the `_events` folder. This will generate an event page and a link on the events list. The address of the event page will be `autonomy-and-verification-uol.github.io/events/` followed by the file's name.

The markdown file should have the following header:

```
---
layout: event
title: "page title"
---
```

Using the `event` layout will add the "Back to Events" link to the top of the page.
The `"page title"` will be displayed at the top of the page.

### External Event Pages

If your event already has an external page hosted elsewhere, but you'd still like it to be included on the lab's events list, then you can add

```
externalURL: "your link"
```

to the header of the markdown file. Here, "your link" should be the url of the external page. This will generate an entry in the events list, but it will simply link to the external page (and an external link icon will show after the name to indicate this to the users).


### Adding an Event Summary

In summary, to add an event page:
1. make a new markdown file in the `_events` folder,
2. add `layout:event` and a `title` to the file's header, and;
3. commit this change to the master branch.

## Adding a New Project

To add a new project to the website's [projects](https://autonomy-and-verification-uol.github.io/projects) page, make a new markdown file in the `_projects` folder (note: not the `projects` folder). This will generate a project description on the projects page. The title of this file should be descriptive, but it's not displayed anywhere on the site.

The file should have the following header:
```
---
title : "project title"
---
```

The `"project title"` will be the header of the project description on the projects page, and the content will appear under this header.

## When a Project Ends

When a project has ended, simply move its description file from `_projects` to `_projects-previous`. This will move the project's description from "Current Projects" to "Previous Projects" on the [projects](https://autonomy-and-verification-uol.github.io/projects) page.

## Managing the Members List

The [Members](https://autonomy-and-verification-uol.github.io/members) page is automatically generated from the data in `_data/members.yml`, which contains three data structures: `CurrentMembers`, `AffiliatedMembers`, and `PreviousMembers`.

A member's record will look like:

```
- name : "member name"
  website: "member website"
  orcid: "orchid url"
```

The `-` indicates that it is an element in the relevant list (of either Current, Affiliated, or Previous Members). The `website` and `orchid` fields are optional.

### Adding a new Lab Members

To add a new member to the members page, you need to add their details to the `_data/members.yml` file.

If they are a 'full' member of the lab, then add their details to the `CurrentMembers` list. Note that `website` and `orchid` are optional.

If they are an affiliated member of the lab, then add their details to the `AffiliatedMembers` list. Each element of this list contains the `Institute` and `MembersList` fields, e.g.:

```
- Institute: "institute name"
  MembersList:
    - name : "member name"
      website: "member website"
      orcid: "orchid url"
```

If the member belongs to an institute that is currently not listed, then use the structure above to add the new institute and the member's details. If the member belongs to an institute already in the list, then simply add their details to the `MembersList` of that institute. Again, `website` and `orchid` are optional fields.

### When a Member Leaves

When a member leaves the lab, simple move the fields containing their data to the `PreviousMembers` list. Again, `website` and `orchid` are optional fields.
