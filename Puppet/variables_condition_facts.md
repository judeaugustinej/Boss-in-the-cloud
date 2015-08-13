> Variables
>> * $variables always start with a dollar sign.

>> * You assign to variables with the = operator.

>> * Variables can hold strings, numbers, special values (false, undef…), arrays, and hashes.

>> * You can use variables as the value for any resource attribute, or as the title of a resource.

>> * You can also interpolate variables inside strings, if you use double-quotes. To distinguish a
${variable} from the surrounding text, you should wrap its name in curly braces.
```
$longthing = "Imagine I have something really long in here. Like an SSH
key, let's say."
file {'authorized_keys':
path => '/root/.ssh/authorized_keys',
content => $longthing,
}
```

>> * Every variable has a short local name and a long fully-qualified name. Fully qualified variables􀀀􀀀
look like $scope::variable. Top scope variables are the same, but their scope is nameless. (For
example: $::top_scope_variable.)
