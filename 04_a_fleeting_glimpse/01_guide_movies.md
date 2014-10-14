**WDI Fundamentals Module 4**

# A Fleeting Glimpse

## Learning Objectives

* Gain exposure to the power at your fingertips
* Get excited about web development

## Outline

We've taken a thorough look at some of the core fundamentals of programming in
the context of Ruby. You must be asking yourself, "All this is well and good,
but what is something that I can actually _do_ with these skills?" That's what
we're going to take a look at now.

For a brief moment, we are going to abandon our pursuit for mastery of our craft
(only for a moment) to get a glimpse of the power that you will soon be weilding
with great precision. For the sake of this unit, do not worry about
understanding everything that you are asked to do. However, pay attention to
following these instructions _precisely_. With a little patience, and some
attention to detail, simply marvel at the ease with which you (yes, **you**) can
spin up an application that exists on the internet!

> Our goal for this unit is to create a web application that allows the users to
> enter a search term and see a list of movies that match the search term.

Navigate to a convenient location on your Nitrous box's terminal (for example,
  `workspace/wdi-fundamentals/`).

Type the following command into your terminal. Remember, only what comes _after_
the dollar sign.

```
$ rails new movies_app
```

Lots of things might have happend! And your computer may be busy for a few
seconds. You just created a new Rails application! It lives inside a folder
called `movies_app`, since that's the name of our application. Enter this newly
created folder.

```ruby
$ cd movies_app
```

Use `ls` to view the contents of this folder. Yes, there's quite a lot of stuff
in here! All these files are components that work together to make a web
application. Remember, it's ok that we don't understand the parts that all of
these files play just yet. For now, let's open up the file called `Gemfile`
(**not** `Gemfile.lock`).

Add the following line to the bottom of your Gemfile.

```ruby
gem 'httparty'
```

This tells our web application that it needs to use a tool called `httparty`.
For this to work, we must also install `httparty`. Do this by running the
following command in your terminal.

```
$ bundle install
```

This may take a moment to finish, but when it does, we will be good to go!

Now, we're going to make use of some nifty Rails tools to quickly set up this
project to be able to handle movies. Run the following commands in your
terminal one after the other to achieve this.

```
$ rails g scaffold movie search:string
$ rake db:migrate
```

That's all of the set up we need to do. Now time to dive into our code.

One of the folders that exists inside our current folder is `app`. Inside `app`,
is another folder called `controllers`. In here, you will find a file called
`movies_controller.rb`. Open up this file in your text editor.

There is already a lot of code in here! This code was written for us by Rails
when we created this application. We need to make some minor modifications to
allow this app to serve our goal.

Find the section of code inside this file that looks something like this.

```ruby
  def create
    @movie = Movie.new(movie_params)

    respond_to do |format|
      if @movie.save
        format.html { redirect_to @movie, notice: 'Movie was successfully created.' }
        format.json { render :show, status: :created, location: @movie }
      else
        format.html { render :new }
        format.json { render json: @movie.errors, status: :unprocessable_entity }
      end
    end
  end
```

We're going to strip out the contents of this "method" (the ten or so lines of
code between the first `def` and the last `end`) and replace it with our own
code. Replace the code inside to end up with a "method" that looks like this.

```ruby
  def create
    url = URI.escape("http://www.omdbapi.com/?s=" + movie_params[:search])
    @movies = JSON.parse(HTTParty.get(url))["Search"]
    render :index
  end
```

This tells our application to look for movies based on the search term on the
[Open Movies Database API](http://omdbapi.com), an open source bank of movie
information.

Next, find and open a file called `index.html.erb`, that lives inside
`app/views/movies`. You should see a file that looks like this.

```html
<h1>Listing movies</h1>

<table>
  <thead>
    <tr>
      <th>Search</th>
      <th colspan="3"></th>
    </tr>
  </thead>

  <tbody>
    <% @movies.each do |movie| %>
      <tr>
        <td><%= movie.search %></td>
        <td><%= link_to 'Show', movie %></td>
        <td><%= link_to 'Edit', edit_movie_path(movie) %></td>
        <td><%= link_to 'Destroy', movie, method: :delete, data: { confirm: 'Are you sure?' } %></td>
      </tr>
    <% end %>
  </tbody>
</table>

<br>

<%= link_to 'New Movie', new_movie_path %>

```

Inside the `<tr>` tags, you will find four `<td>` tags. Delete the tags that
`Show`, `Edit`, and `Destroy`. We won't be needing them. Your file should now
look like this.

```html
<h1>Listing movies</h1>

<table>
  <thead>
    <tr>
      <th>Search</th>
      <th colspan="3"></th>
    </tr>
  </thead>

  <tbody>
    <% @movies.each do |movie| %>
      <tr>
        <td><%= movie.search %></td>
      </tr>
    <% end %>
  </tbody>
</table>

<br>

<%= link_to 'New Movie', new_movie_path %>
```

Next, in the only remaining `<td>` tag, change `movie.search` to `movie["Title"]`

```html
<h1>Listing movies</h1>

<table>
  <thead>
    <tr>
      <th>Search</th>
      <th colspan="3"></th>
    </tr>
  </thead>

  <tbody>
    <% @movies.each do |movie| %>
      <tr>
        <td><%= movie["Title"] %></td>
      </tr>
    <% end %>
  </tbody>
</table>

<br>

<%= link_to 'New Movie', new_movie_path %>
```

Make another `<td>` tag right under that one, except this one should contain
`movie["Year"]`. Your file should now look like this.

```html
<h1>Listing movies</h1>

<table>
  <thead>
    <tr>
      <th>Search</th>
      <th colspan="3"></th>
    </tr>
  </thead>

  <tbody>
    <% @movies.each do |movie| %>
      <tr>
        <td><%= movie["Title"] %></td>
        <td><%= movie["Year"] %></td>
      </tr>
    <% end %>
  </tbody>
</table>

<br>

<%= link_to 'New Movie', new_movie_path %>
```

Excellent! Believe it or not, our app is ready to go!

Start up your application by running the following command in your terminal.

```
$ rails server
```

Your terminal will now show you some messages regarding the server, and will
not display a prompt for you to type more commands. This is ok. This is because
our server is running! If you wish to shutdown the server, you can use `Ctrl-C`.

To view your web application, select `Preview` from the top menu of your Nitrous
IDE, and inside, select `Port 3000`. This should take you to what looks like a
Rails welcome page.

To the URL in your browser, add `/movies/new` and hit Enter. For example, if
your URL was `http://wdi-fundamentals-154576.use1-2.nitrousbox.com`, you should
visit the URL `http://wdi-fundamentals-154576.use1-2.nitrousbox.com/movies/new`.

There's a search form for you to look for movies! Go ahead, try it. Enter a
word or phrase to search for, and click the Button (or simply press Enter). You
should see a list of movies that your application found on the internet!

Clicking 'New Movie' at the bottom of the results page should take you back to
your search form!

As long as your server is still running, you can send this URL to all of your
friends, and they should be able to use your application, no matter where they
are! Such is the joy and wonder of web development. Get excited, and happy
coding!
