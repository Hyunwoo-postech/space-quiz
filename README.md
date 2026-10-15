# Orbit - Space Quiz

Orbit is a self-contained, single-page space exploration quiz. Answer 10
randomly ordered questions, learn from explanations after each answer, and see
your final score. Restart to try again with a newly shuffled question order.

The app uses semantic HTML, inline CSS, and vanilla JavaScript in `index.html`.
It supports light and dark color schemes, reduced motion, and keyboard navigation.
There are no dependencies, backend services, or build steps.

## Run locally

Clone this repository and open `index.html` in a modern web browser. No package
installation or local server is required.

To check changes, play through correct and incorrect answers, finish the quiz,
and restart. Also check a narrow viewport and light/dark color schemes when
changing the layout or styling.

## GitHub Pages

The site is published at <https://hyunwoo-postech.github.io/space-quiz/>.

In the repository's **Settings > Pages**, the build and deployment source must
be **GitHub Actions**. The workflow in `.github/workflows/pages.yml` packages
only `index.html` as the site artifact; no compilation is needed.

Pull requests targeting `main` run the packaging job without deploying. Pushes
to `main` publish the site through the `github-pages` environment. You can also
redeploy `main` from the Actions tab using **Deploy GitHub Pages > Run workflow**.
