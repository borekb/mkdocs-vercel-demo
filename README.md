# MkDocs on Vercel

Demo of how to deploy MkDocs site to Vercel (formerly ZEIT Now).

## How to deploy

Just run `now` in this folder. (Tested as of `now@19`.)

## Details

Note that for local development (`yarn dev`), Docker container is used so that it's not necessary to have Python and all the right extensions locally.

For cloud deployment, the two key parts are:

- The `requirements.txt` file – Vercel will see it and treat the deployment as a Python project.
- The `build` script in `package.json` – Vercel runs it on deployments. Note that this is _not_ dockerized.
