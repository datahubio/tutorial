# Tutorial: Publishing data rich documents on DataHub Next

Hi, welcome to DataHub Next : ). In this tutorial we are going to cover the basics of publishing a data rich document on our initial version of DataHub Next.

### But wait, what is a data rich document?

A data rich document is a document in which the writer can easily mix formatted text content with data visualizations. This means that you don't have to code nor embed your charts and tables, those can be added to the document with a very simple syntax, passing inline-data or simply referencing your data files. What you end up with is a plain text, human-readable document which is simple to edit and looks awesome when rendered in DataHub Next!

### What does this syntax looks like?

The structure and text formatting of the documents are created with markdown (take a look at [this guide](https://www.datopian.com/playbook/markdown) to learn more about markdown). But it's not simply markdown, it's markdown on steroids: writers are capable of easily adding tables of content, mathematical formulas, data visualizations and more!

And guess what? What you are reading right now is a data rich document powered by DataHub Next, that's why we can do this:

=> INSERT LINE CHART HERE

Awesome, right? Even more awesome is that this chart is created by simply having the following snippet in this document:

```
=> INSERT SNIPPET HERE
```

You can check out the full source of the data rich document you are reading [here]().

More on how to create charts and tables later, but now, this must be coming from somewhere, right?

### What is a DataHub Next project?

A DataHub Next project is simply a GitHub repo with a README and, potentially, data files. That's right: you can take advantage of everything that GitHub offers in terms of revisioning, changes history and so on and transform your repo into a data rich document.

Imagine how cool it would be to store your reports, datasets and analysis in this format. Now, let's learn how to actually do it.

## Create a GitHub repo

First, create a repo under your organization or user in GitHub. DataHub Next currently does not support private repos, make sure this new repo is public and that your main branch is named "main" (updates on this coming soon).

## Push a README.md file to the repo

Now, create a README.md file. In this file, feel free to use anything that markdown has to offer. For this tutorial, we are going to use the following basic structure:

```markdown
# Personal monthly costs 2023

This is the tracking of my personal monthly costs on 2023.

## Table

## Chart

```

### Tables

Let's add a table to the README file. There are different ways to specify the data that's going to be displayed on the table.

You can specify `data` and `cols`, like that:

```
=> INSERT TABLE SNIPPET HERE
```

Or you can pass inline CSV data to the table:

```
=> INSERT TABLE SNIPPET HERE
```

Or you can specify a url to a CSV file, which can be a relative link to a file in your repo (e.g `data.csv`) or an external URL:

```
=> INSERT TABLE SNIPPET HERE
```

For this tutorial, let's go with the first option, so, under the `## Table` header in your file, add the following snippet:

```
=> INSERT TABLE SNIPPET HERE
```

Note that tables can also be made full width by setting the `fullWidth` property:

```
=> INSERT TABLE SNIPPET HERE
```

Check out how this looks when rendered:

=> INSERT FULLWIDTH TABLE HERE

### Graphs

Now, let's add a graph to the README file. There's a variety of ways to create charts in DataHub Next.

For charts that demand more customization, the Vega and VegaLite components can be used:

```
=> INSERT VEGA SNIPPET HERE
=> INSERT VEGA LITE SNIPPET HERE
```

To keep it simple, we are going to use the LineChart component on this tutorial. Add the following snippet to your README file under the `## Chart` header:

```
=> INSERT LINECHART SNIPPET HERE
```

This is going to look like this when rendered:

=> INSERT LINECHART HERE

And just like for tables, line charts can also be made full width, check out how this same line chart looks like with the `fullWidth` property:

=> INSERT FULLWIDTH LINECHART HERE
  

### Final document

At this point, your document should look like this:

```
=>  FULL README 
```

We now have a README file ready to be used on DataHub Next, let's visualize our creation.

## Go to your project's page on DataHub

It's time to check the results. In order to do that, edit the following URL, replacing `{owner}` with your user or org id and `{project}` with the name of your repo:

datahub.io/@{owner}/{project}

Finally, access the URL.

___

Cool, isn't it? Get in contact with us and let us know what you think!

