# v0.x Wekan fork upcoming release, already committed to devel branch

This release adds the following new features:

* Start- and Duedate for cards;
* Allow IE 11 to work;
* Option to hide system messages in the card;
* Option to setup minimum limit to show cards count
  for each list in board;
* Option 'filter by empty' to filter by cards by 'no member'
  and 'no label' properties;
* Speedup: Added MongoDB index on CardId into Comments collection.

and fixes the following bugs:

* Sandstorm: username handling, restore identity, eslint regressions,
  board not found;
* Failure to load when navigator.language is Chinese or Finnish;
* Hover background for labels in filter sidebar. Now correctly
  centered;
* Display message when user wants to choose existing username;
* Client sometimes fails to receive current user's profile;
* Old users could see broken presence indicators on new users.

Thanks to GitHub users dwrencha, fmonthel, mario-orlicky, pierreozoux,
shoetten, and xet7 for their contributions.

# v0.11

This release adds the following new features:

* Notification system with email notifications of the changes in a board,
  a list or on a card;
* Show the exact time when hovering the activity time;
* Allow to edit more easily longer card titles by resizing the input box;
* Add shortcuts to move cards to the top or the bottom of a list;
* Add a warning indicator when the application is offline;
* A new log-in button on the public board view to sign in, even if the board
  is published;

and fixes the following bugs:

* Fix the syntax of the `docker-compose.yml`;
* Use the correct pluralization of emoji;
* Only publish required user data and keep the hashed passwords confidential;
* Fix the generation and alignment of the initials avatars;
* Fix the “welcome board” feature;
* Only display the buttons in the board header, if the data is available
  and the user is able to use it;
* Fix the scaling of cover images;
* Fix bugs on Internet Explorer v11 that blocked card creation and activity feed
  visualization.

Thanks to GitHub users alayek, AlexanderS, choclin, floatinghotpot, ForNeVeR,
PeterDaveHello, seschwar, and TheElf for their contributions.

# v0.10.1

This patch release fixes two bugs on Sandstorm:

* Drag and drop was broken;
* Avatars weren’t working.

# v0.10

This release features:

* Trello boards importation, including card history, assigned members, labels,
  comments, and attachments;
* Invite new users to a board using a email address;
* Autocompletion in the minicard editor. Start with <kbd>@</kbd> to start a
  board member autocompletion, or <kbd>#</kbd> for a label;
* Improve the user interface on small screens so that Wekan could be used on the
  mobile web;
* Accelerate the initial page rendering by sending the data on the intial HTTP
  response instead of waiting for the DDP connection to open;
* Support images attachments copy pasting;
* On Sandstorm, expose the Wekan grain title and URL to the Sandstorm shell;
* Support Wekan deployment under a sub-path of a domain name.

New languages supported: Arabic, Catalan, Italian, and Russian.

Thanks to GitHub users AlexanderS, fisle, floatinghotpot, FuzzyWuzzie, mnutt,
ndarilek, SirCmpwn, and xavierpriour for their contributions.

# v0.9

This release is a large re-write of the previous code base. This release marks
the beginning of our new user interface and continues to improve the overall
performance and security. It also features the following improvements:

* A new user account system, including the possibility to reset a forgotten
  password, to change the password, or to enable email confirmation (all of
  which were previously impossible);
* Avatar customization, including the possibility to upload images and to choose
  one from Gravatar or the user initials (on Sandstrom we use the avatar exposed
  by Sandstorm);
* Cards multi-selection to facilitate batch actions such as moving all the cards
  of selection, or attaching a label or a member to them;
* Automatic drafts saving synced with the server;
* Keyboard navigation, press `?` to read the list of available shortcuts;
* The possibility to restore archived boards, lists, and cards.

Starting from this release we will also distribute official docker images on
both the [GitHub release page](https://github.com/wekan/wekan/releases) and on
the [DockerHub](https://hub.docker.com/r/mquandalle/wekan). We also configured
Heroku one-click install and improved Sandstorm integration with the integration
of its build-in sharing model.

New languages supported: Chinese, Finnish, Spanish, Korean, and Russian.

Special thanks to GitHub users ePirat, nata-goddanti, ocdtrekkie, and others who
have supportive during this *traversée du desert*, and to neynah for the Wekan
icons.

# v0.8

This release continues the implementation of basic features of a “kanban”
software, especially:

* Basic card attachments. If the attached file is an image we generate and
  display a thumbnail that can be used as a card “cover” (visible in the board
  general view);
* User names mentions and auto-completion in card description and comments
  (though we don’t have any notification system for now, making this feature a
  less useful that it should);
* Filter views, current filtering options are based on labels and assigned
  members;
* Labels creation and suppression at the board level (previously we had a fixed
  list of labels);
* Customization of the board background color.

This release is also the first one to introduce localization of the user
interface.

New languages supported: French, German, Japanese, Portuguese, and Turkish.

# v0.7.1

This release fixes the following bugs:

* Unexpected lost of the card sorting on the server side;
* Fix a bug during board creation;
* Focus the new list form if the board is empty.

# v0.7

This release starts the transition from a toy project to something useful. Along
with some security and performance improvements (for instance, opening a card
used to take a long time because it was re-generated the entire DOM whereas only
the popover was new). New features includes:

* Add and remove labels to cards;
* Assign and unassign members to cards;
* Archive cards (though restoration is not yet possible);
* Board stars;
* Markdown and emoji support in comments and card description;
* Emoji auto-completion in the text editor;
* Some keyboard shortcuts (eg `Ctrl`+`Enter` to submit a multi-line input).

We also introduced basic support for the [Sandstorm](https://sandstorm.io)
platform, and distribute a `spk` (Sandstorm PacKage) for this release and
subsequent.
