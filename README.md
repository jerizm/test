#Unit Testing

##xUnit.net

###Data Driven
```C#
    [Theory,
    InlineData("goodnight moon", "moon", true),
    InlineData("hello world", "hi", false)]
    public void Contains(string input, string sub, bool expected)
    {
        var actual = input.Contains(sub);
        Assert.Equal(expected, actual);
    }
```

###Exceptions
```C#
Exception ex = Assert.Throws<AuthenticationException>(() => services.Authenticate("user", "wrong"));
```
