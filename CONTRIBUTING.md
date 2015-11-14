## Contributing

### Reporting bugs / Requesting features

For practical reasons we only accept issues that are bug reports or feature requests. Make sure to read the following guidelines before opening new issues.

#### :mag_right: Avoid duplication

You'd help us out a lot by first checking if someone else has reported the same issue. Moreover, the issue may have already been resolved with a fix available.

#### :heart: Make it eazy

Share as much information as possible. Include operating system and version, browser and version, version of Citizens. Also include steps to reproduce the bug and any logs from browser and/or process whenever possible.

A good approach to a bug report is being very clear on how to reproduce it. Example:

> 1. Run app with `rails server`
> 2. Navigate to `/users/new`
> 3. Click on `button` and see error in `terminal` output
> 
> Results: What is the actual result that makes it a bug? (e.g: Misaligned text in header, see attached snapshot, etc.)
> 
> Expected results: What should it look like? (e.g.: text in header should be aligned with dropdowns, etc.)


### :fork_and_knife:  Pull requests

#### 1. Fork

To contribute code, start by forking our repo on github. You'll get something like this:
```
https://github.com/{your-user}/citizens
```

#### 2. Clone

Then clone your fork:
```sh
$ git clone git@github.com:{your-user}/citizens && cd citizens/
```

> **Note**: `$` is the terminal. You don't need to copy it.

#### 3. Add remote repo

Add the official repo as a remote, to track changes:
```sh
$ git remote add upstream git@github.com:CitizensProject/citizens.git
```

#### 4. Create your new branch

Create a new branch for the changes you are going to contribute, with a relevant name. Some examples:
```sh
$ git checkout -b feature/some-new-stuff
$ git checkout -b fix/some-bug 
$ git checkout -b remove/some-file
```

#### 5. Make your changes

Make your changes using your favorite editor. In my case [Atom.io](https://atom.io/).

#### 6. Commit your changed files

Once you're done making your changes, run:
```sh
$ git add somefile.txt
$ git commit -a -m "Adding somefile.txt"
```

#### 7. Prepare your code for push

When you think your code is ready, prepare for pushing the code by first getting the changes from the main repo:
```
$ git pull --rebase upstream development
```
(You may need to solve any conflicts from the rebase at this point)

#### 8. Push your commits

After that you can push the changes to your fork, by doing:
```
git push origin feature/some-new-stuff
git push origin fix/some-bug
```

#### 9. Push your commits

Finally go to `https://github.com/CitizensProject/citizens` in the browser and issue a new pull request. Github normally recognizes you have pending changes in a new branch and will suggest creating the pull request.

Main contributors will review your code and possibly ask for changes before your code is pulled in to the main repository. We appreciate your time and efforts!

#### General guidelines

* Do not make a pull request withouth having run the app on your own. This means, you have to at least [smoke test](http://en.wikipedia.org/wiki/Smoke_testing_(software)) what you did. 
* Try not to pollute your pull request with unintended changes. Keep them simple and small. Unrelated commits will prevent us from merging.
* Pull requests should always be against the `development` branch, never against `master` or `staging`.
* All pull requests must comply with the project's coding styles explained here.

### :pencil2: Coding style

#### GIT conventions
In general terms, we agree with almost everything said in this [blog post about GIT conventions](https://medium.com/code-adventures/a940ee20862d) and so should you. We only add/differ the following:

* Commits should try to be as simple (atomic) as possible, but not simpler. Meaning you should always be able to revert specific `fix`es, `edit`s, `update`s, `add`s, and `remove`s with `git revert`

#### Rules

* Two spaces for indentation, never tabs.
* Double quotes only, never single quotes. Use simple quotes only in double quotes.
  
  *Example*:
  ```ruby
  example = "This is an example. #{@example.present? ? @example.id : 'Not ID'}"
  ```
* Avoid trailing whitespace. Blank lines should not have any space.
* The last line of the file allways blank.
