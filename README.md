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
2. Obtain your Google Scholar profile ID and copy it.

![Google Profile ID](https://raw.githubusercontent.com/JJ/cv/master/img/marie-curie-id.png)

3. Paste that id in the `myId` variable in the YAML preamble to the RMarkdown
   file (don't worry about that if you don't understand, just paste the ID in
   [this line](https://github.com/JJ/dynamic-academic-cv-template/blob/95157f5627223d26d6362a366e963e21e09b252f/academic-cv-summary.Rmd#L9)

```yaml
myId: EmD_lTEAAAAJ
```

4. Save, commit and push (that will be done automatically for you if you're
   using the web interface)

```shell
git commit -am "Use my own ID" && git push
```

5. Navigate to the last action in the *Actions* menu, the one on top, such as
   [this
   one](https://github.com/JJ/dynamic-academic-cv-template/actions/runs/4487482539). The
   PDF for your CV will be in a zip file that you can download clicking in
   `academic-cv`, such as [this one](https://github.com/JJ/dynamic-academic-cv-template/suites/11725063370/artifacts/610441418)

You have any problem, just [raise an issue](https://github.com/JJ/dynamic-academic-cv-template/issues)

## More advanced usage

