# Dynamic academic CV template

Repo template for a dynamically generated academic CV (scraped from Google
Scholar). This template uses the [`scholar` R
package](https://cran.r-project.org/web/packages/scholar/index.html) to
dynamically generate a CV based on publications in the Google Scholar profile.

## Basic instructions

> These instructions assume that you have a [GitHub](https://github.com)
account, and have basic knowledge on how to use it, from the web, desktop or
command line.

1. Click on "Use this template" in the button row above to create a repo with
   this template.
2. Change the `author` field to your name

    ```YAML
    author: "Marie Skłodowska-Curie"
    ```

3. Obtain your Google Scholar profile ID from the URL of your profile and copy it.

    ![Google Profile ID](https://raw.githubusercontent.com/JJ/cv/master/img/marie-curie-id.png)

4. Paste that id in the `myId` variable in the YAML preamble to the RMarkdown
   file (don't worry about that if you don't understand, just paste the ID in
   [this line](https://github.com/JJ/dynamic-academic-cv-template/blob/95157f5627223d26d6362a366e963e21e09b252f/academic-cv-summary.Rmd#L9))

    ```yaml
    myId: EmD_lTEAAAAJ
    ```

Change also the default pronoun just below. It defaults to `her`

    ```yaml
    myPronoun: her
    ```

5. Save, commit and push (that will be done automatically for you if you're
   using the web interface)

    ```shell
    git commit -am "Use my own ID" && git push
    ```

6. Navigate to the last action in the *Actions* menu, the one on top, such as
   [this
   one](https://github.com/JJ/dynamic-academic-cv-template/actions/runs/4487482539). The
   PDF and DOCX for your CV will be in a zip file that you can download clicking in
   `academic-cv`, such as [this
   one](https://github.com/JJ/dynamic-academic-cv-template/suites/11725063370/artifacts/610441418)

> The first run will take north of 10 minutes. The cache will kick in after
that, resulting in a duration of around 3 minutes.

The curriculum will be also auto-generated every 1st and 15th of every
month. You'll get an email from GitHub when this happens. After 60
days, scheduled actions are disabled, so you will need to make some
change in the repo to continue generation for other 60 days.

You have any problem, just [raise an issue](https://github.com/JJ/dynamic-academic-cv-template/issues)

## More advanced usage

The installed R packages include the above mentioned `scholar`, as well as
`ggplot2` for plotting and `dplyr` for processing. You can edit either the text
or R chunks of [`academic-cv-summary.Rmd`](academic-cv-summary.Rmd) at will; the
new version will be generated when you push changes to `main`, and thereafter
every 15 days (or so).

You can also set up your own repo from [one of the
releases](https://github.com/JJ/dynamic-academic-cv-template/releases),
customizing every bit, or adding a bibliography file (which, unfortunately,
can't be easily generated automatically from the profile).

## LICENSE

This template has been released under the [Affero GPL license](LICENSE)
