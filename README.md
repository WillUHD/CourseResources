# GPAResources
Continuously updated course profile of SHSID's new curriculums for the GPA Calculator app

### `./Courses.gpa`
- This is the current course profile for SHSID's high school, and will be continuously updated
- **LAST UPDATE**: `April 1, 2026`
- Written in a custom JSON DSL with full-line comment support.
- Resources (via gh-proxy mirror) is used by the [GPA Calc app](https://apps.apple.com/us/app/gpa-calculator-by-michel/id1540111715) 
- Original app made by [MichelG](https://github.com/michelg10/), updated by me, contributions made by [ziqian-huang0607](https://github.com/Ziqian-Huang0607)

### GPA Calc's logic
- The app will download the continuously updated configuration file from here to use in its own UI.
- So, in theory, the app's physical code doesn't have to be updated. Only the course profiles have to, and the resources will automatically be updated by the app.

### View the resources
- View the source for the current configuration profile (last updated spring 2026 by willuhd) [here](https://raw.githubusercontent.com/WillUHD/GPAResources/refs/heads/main/Courses.gpa)
- View the gh-proxy mirror for the profile [here](https://edgeone.gh-proxy.org/https://raw.githubusercontent.com/WillUHD/GPAResources/refs/heads/main/Courses.gpa) (makes the profile available in mainland China)
