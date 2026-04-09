# CourseResources
Continuously updated course profiles and catalogs of SHSID's curriculums for curriculum services. 

### `Courses.gpa` (last update: `April 1, 2026`)
- This is the current profile for SHSID used for the GPA Calculator (iOS and web) projects, and will be continuously updated
- Written in a custom JSON DSL with full-line comment support.
- Resources (via gh-proxy mirror) is used by the [GPA Calc app](https://apps.apple.com/us/app/gpa-calculator-by-michel/id1540111715) 
- Original app made by [MichelG](https://github.com/michelg10/)
- Reworked by me (to include remote update functionality, rule checking, configurable score maps), with some IB contributions by [ziqian-huang0607](https://github.com/Ziqian-Huang0607)

### `Courses.catalog` (last update: `April 10, 2026`)
- The catalog file used for SHSID's interactive course planner (made by Indexademics)
- Currently in alpha! PRs NOT(!!!) welcome we are sTILL testing; contact me in person if something is really wrong.

### How all this works
- The client (iOS/serverless web) will download the continuously updated configuration file from here to use in its own UI.
- This way the app's physical code doesn't have to be updated. Only the course profiles have to, and the resources will automatically be updated by the app. This mainly streamlines development for course tools as the course catalog may change much more frequently than these tools (if at all).
- I'm the primary maintainer of these course configurations and this repository serves as the hosting point for all of them. They may contain contributions made by many people, credits given as-is in the files themselves (in a credits section or commented). For future SHSID course profile projects that need hosting, adding to this repository is recommended over making another one. 

### View the resources
- For production (eg. iOS/web GPA Calculators), the EdgeOne mirrors are used. This makes the content accessible worldwide, including mainland China.
- `Courses.gpa` as raw [here](https://raw.githubusercontent.com/WillUHD/CourseResources/refs/heads/main/Courses.gpa), gh-proxy mirror [here](https://edgeone.gh-proxy.org/https://raw.githubusercontent.com/WillUHD/CourseResources/refs/heads/main/Courses.gpa)
- `Courses.catalog` as raw [here](https://raw.githubusercontent.com/WillUHD/CourseResources/refs/heads/main/Courses.catalog), gh-proxy mirror [here](https://edgeone.gh-proxy.org/https://raw.githubusercontent.com/WillUHD/CourseResources/refs/heads/main/Courses.catalog)
