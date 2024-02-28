# Contributing to MyFinances

Welcome to our project! We appreciate your interest in the project, and the chance you may help contribute!
Okay... so how do I get started!?

## Getting your environment setup

To contribute to our application, you'll need to see changes be made. For this, you won't be able to see them on the
production build. You'll have to setup the project on your local machine.

To setup the project, we have a set **Getting Started** guide!

<tip>
    We highly encourage the Jetbrains products in this project, as PyCharm Professional does have great django support.
    Things like `starting + stopping dev server with one click`, `running tests with one click`, `viewing documentation`,
    `nice templating`, `orm support`, `quick interactions` and more! But, you don't have to use Jetbrains, feel free to use 
    any IDE which better suits you!
</tip>

## Suggesting a new feature

Got a new feature idea? That's amazing, we love new ideas, however big or small! To tell us about your idea,
we suggest you make an **issue** on github. These can be found here:
[https://github.com/TreyWW/MyFinances/issues/new/choose](https://github.com/TreyWW/MyFinances/issues/new/choose)

Here you can choose what kind of issue you have, in this case you'll choose either of these:

- **Feature Request**: This is if you are requesting for **somebody else to add this feature** (or you just want to
  discuss the IDEA of a feature)
- **Feature**: This is if you would like to **work on the feature yourself**. We suggest getting approval for the
  feature before
  working on the code, just in case we decide it's not the best fit.

## Start working on the code

Okay cool, you're now ready to start working on code. Once you have setup the project, you can continue.
So first you'll need a feature to work on. Find an _unassigned_ feature on the Issues tab on github,
once you have found one that is _unassigned_, add a comment to that issue asking to be assigned. This will prevent other
developers from adding this before you finish or the issue being closed.

So now you'll want to create a **new branch**, to store all of your changes while you build out this feature.

We suggest using the branch names: `feature/<xyz>` for features, or `enhance/<xyz>` for improvements.

Now you can get cracking, add them features! Make sure to commit your changes every now and then in case you need to
rollback.

Before Pull Changes, you'll want to test your new features and format the files.

<code-block lang="bash" collapsible="true" collapsed-title-line-number="4">
    # first time running tests
    poetry install --with dev # installs djlint and black
    # run tests
    python manage.py test --parallel
    djlint ./frontend/templates --reformat
    black ./
</code-block>

<deflist type="full" collapsible="true">
    <def title="python manage.py test">
        This is used for actually testing our application, these are some tests we manually created to make sure our application
        works as expected.
        <tip>
            <code>--parallel</code> is <control>NOT</control> needed, it simply runs multiple tests at a time to speed things up.
        </tip>
    </def>
    <def title="djlint ./frontend/templates --reformat">
        This is used to reformat the HTML files, as they can become messy. Running without <code>--reformat</code> will
        allow you to just preview what is incorrectly formatted.
    </def>
    <def title="black ./">
        This is used to reformat the PYTHON files, as they can also become messy.
    </def>
</deflist>

## Pull in your changes

What's a PR? A Pull Request is a way of merging your local, forked code, into our shared official repository.
You can [create a PR here](https://github.com/TreyWW/MyFinances/pulls), but if you go to 
[our repository home](https://github.com/TreyWW/MyFinances) you should see a big yellow box asking
"would you like to merge _your branch name_ into _main_?", you can just press "Pull In".

After this, make sure to include as much detail as possible in your PR, especially about tests.
We would like 100% test coverage if possible for any new functions, views, and any other backend code you add.|

That's about it! If you struggle at any parts, and just need a bit of support you can either
join our [discord server](https://discord.gg/YDQq2uc2ap) or create an Issue/PR and mention that you need help.

Good luck! Have fun, don't stress if you need to take a break or need help, just speak to us!