# Lighthouse

(Formerly "*Beacon Enhancement Suite*", "*BES*".)

## Requirements

- [Google Chrome Browser](https://www.google.com/chrome/browser/desktop/index.html "Download Google Chrome")
- NSW SES Beacon Account

## Purpose

Lighthouse is intended to augment the functionality provided by Beacon. It streamlines some common workflows, such as closing a job, or tasking a job to a team. 
It also provides customised displays for use on screens in an Operations Room.

Lighthouse also provides an opportunity to test functionality or fixes before those changes are put to the Beacon development team for incorporation into the core system.

## Operation

Lighthouse is completely client-side. It stores no user data and runs completely within the Chrome web browser. It is bound by existing Beacon management systems, such as user permissions, security checks and logging of actions within Beacon for auditing purposes.

Lighthouse simply interfaces with the same information and functionality as normal Beacon, just in a different (and hopefully more effective and efficient) way.

## Usage

A compiled stable version of the Lighthouse system is available through the [Google Chrome Store](https://chrome.google.com/webstore/detail/lighthouse/eheijalihofgiaoeanmnjceefmcpajnb "Lighthouse in the Google Chrome Store").

This version is updated when major changes are committed through the GitHub repository, and/or it is convenient and safe to distribute an updated version.

A compiled developer version of the Lighthouse system is available through the [Google Chrome Store](https://chrome.google.com/webstore/detail/lighthouse-development-pr/jcmiinngebdojjbcjlpjpdhiankmjbda "Lighthouse Development Preview in the Google Chrome Store").

This version is updated when minor changes are committed through the GitHub repository, and/or there is something in the pipeline that we want to test on a wider audience.

## Development

Install:

- Node and NPM (tested with v18) `brew install node`
- `cd Lighthouse`
- `npm install`

Build for development:

- `npm start`
- The extension should now be built into `dist/`. Load this into Chrome with dev mode turned on.
- Webpack should automatically rebuild as you make changes but some changes won't take effect in Chrome until you reload the extension.

Pull requests are welcome!

## Known Limitations

- All summary, statistics and export screens will only follow HQ and time/date filters, eg if you filter by job type then generate a summary it will be everything not just that job type.
- Lighthouse menu - If you are a region user it will only show your region, not all units within your region. You need to generate these screens from the Job Register to get around this.
