do-go-ssh
=======

do-go-ssh is a tool for which creates `ssh` hostname rules from your DigitalOcean servers for easier connection. For example, if you have a droplet in DigitalOcean with hostname `foo`, you will be able to connect to `foo` with command `ssh foo` after running the do-go-ssh tool. All you need is an API key with read access from `https://cloud.digitalocean.com/settings/applications`. If you don't want to memorize the API key every time you can also create a `.profile` (or `.bashrc` depending on your platform) function as so:

    function do-go-ssh { PATH_TO_DO-GO-SSH YOUR_API_KEY; }
    export -f do-go-ssh

For example, mine looks like this

    function do-go-ssh { ~/Github/do-go-ssh/do-go-ssh e1aa1...; }
    export -f do-go-ssh

After running `do-go-ssh` you can now connect to your droplet with its hostname. For example, we can now reach our `foo` server with `ssh foo`. Everytime you create a new droplet you have to re-run the tool.

##What operating systems does it support?

MacOSX, at least. And all other operating systems which have ssh config file located at `~/.ssh` should work as well.

##Why you made this?

I personally manage a bunch of DO servers and some of them are located behind a proxy server. With this awesome tool of mine, I'm able to connect to servers with ease.

##License

MIT