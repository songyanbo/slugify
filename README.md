Slugify [![Build Status](https://secure.travis-ci.org/slugify/slugify.png?branch=master)](http://travis-ci.org/slugify/slugify)
=======

SEO-friendly URLs with Slugify

Notice
------
If you want to use it directly in your JSP, take a look into [jstl][1]

Usage
-----
If you want to use Slugify in your Java code you only need the library itself.
Here's the dependency information for Maven:

    <dependency>
		<groupId>com.github.slugify</groupId>
		<artifactId>slugify</artifactId>
		<version>2.1.0</version>
    </dependency>

Now you're able to use it:

    Slugify slg = new Slugify();
    // Result: Hello-world
    String s = slg.slugify("Hello, world!");

You can set custom replacements for Slugify:

    Slugify slg = new Slugify();
    slg.setCustomReplacements(new HashMap<String, String>() {{
    	put("foo", "bar");
    }});

    // Result: Hello-bar
    String s = slg.slugify("Hello foo");

[1]: http://github.com/slugify/slugify/tree/master/jstl
