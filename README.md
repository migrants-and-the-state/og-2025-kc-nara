# og-template

template repository for aperitiiif batches of a files for migrants and the state neh grant project 🥂

## description

this is a modified aperitiiif batch repo. because of the size, images are not stored cannonically in the repo and processed by the github `publish-batch` action. 

instead, cannonical pdfs and images are stored in an NYU Research Workspace (RW) volume. the rake tasks in `lib` process the files from the volume mounted locally and sync the generated image and json resources for the IIIF APIs directly to AWS S3 using credentials stored (and gitignored) in `.env`.

the github action is used to deploy the results to github pages only.

## owner(s)
- [@mnyrop](https://github.com/mnyrop)

## set up

### prerequisites
- git
- asdf

### steps
1. connect to m/s [research workspace mount](https://github.com/Migrants-and-The-State/playbook/blob/main/docs/research-workspace.md)
2. clone repo and `cd` into it
3. install ruby version and gems
    ``` sh
    asdf install ruby
    bundle install
    ```
4. check for available tasks
    ``` sh
    bundle exec rake --tasks
    ```