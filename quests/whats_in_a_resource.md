# What's in a resource?

For Puppet, anything on your system you might want to manage can be represented
as a resource. Puppet has built-in resource types to cover most aspects of a
system an administrator might care about. Some of the most common resource
types are `file`, `package`, `user`, and `service`.

Use the `puppet resource` tool to look at a `file` resource on your system. In
the terminal to the right, enter the following command:

    puppet resource file /tmp/hello_puppet.txt

The block of you see is called a resource declaration—it's how Puppet sees the
world. Resource declarations have a common syntax no matter what you want to
manage and what operating system you're working on.

```puppet
type { 'title':
  parameter => 'value',
}
```

The file resource for `/tmp/hello_puppet.txt` only has one parameter value
pair: `ensure => absent`. The `ensure` parameter expresses the basic state of
the resource. In this case, the `absent` value means that the file specified by
the resource title doesn't exist.

Continue on to the next task, and you'll see how to create this file by
modifying the resource declaration.
