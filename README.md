# Flatiron Workshop Template

## Generating New Workshops

To create a new workshop from a template, run:

```sh
npx create-react-app workshop-name --use-npm --template cra-template-flatiron-workshop
```

This will create a new workshop repo with some starter code and all the
necessary dependencies. It also provides a README with student-facing
instructions for getting the workshop set up locally.

> NOTE: The script above uses npm instead of yarn as the default package
> installer. There are some dependency issues with yarn that need some further
> investigation; in the meantime, npm works just fine.

## Workshop Features

In the workshop repo, the folder structure looks like this:

```txt
.
├── public
└── src
    ├── __tests__
    │   └── 01.test.js
    ├── exercise
    │   ├── 01.js
    │   └── 01.md
    ├── solution
    │   ├── 01.extra-1.js
    │   └── 01.js
    ├── index.js
    └── setupTests.js
```

Under the hood, the workshop repo uses code from
[https://github.com/ihollander/workshop-app](https://github.com/ihollander/workshop-app)
to generate routes for each exercise based on the filenames in the
`src/exercise` and `src/solution` folder. You'll see the `workshop-app` code
referenced in `src/index.js`.

## Adding Exercises

To add new exercises, create the following file using the following naming
convention/folder structure:

- `src/exercises/02.md`: a readme for the exercise.
- `src/exercises/02.js`: starter code for the exercise. **You must have one
  default export in this file!**.
- `src/solutions/02.js` (optional, but encouraged): solution code for the
  exercise.
- `src/solutions/02.extra-1.js` (optional): extra credit solution code. You can
  add multiple extra credit solutions, if you like, by following the naming
  convention `{exercise}.extra-{number}.js`.
- `src/__tests__/02.test.js` (optional): test code for the exercise.

You'll need to restart the app any time you add a new file (otherwise, changes
to the files will hot reload as normal).

## Student Setup

- instructions in the README for running the workshop on the student's computer
- first time doing it, good to talk to the students about how the workshop is
  set up
  - they should run it in the browser, and read the exercise instructions in the
    README
  - they can view a demo of the working solution in the browser to see what the
    end result should be
  - they should write code in the `exercise/01.js` file by following the
    comments
  - they shouldn't look at the solution code unless they're really stuck
