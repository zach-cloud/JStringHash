# JStringHash
This Java project contains classes to compute and brute force StringHashes.

A StringHash is a computation of the SStrHash2 of a String. This is used in the WarCraft III native "StringHash", hence the name of the utility.

# Importing

```$xslt
<dependency>
    <groupId>com.github.zach-cloud</groupId>
    <artifactId>JStringHash</artifactId>
    <version>1.1</version>
</dependency>
```

# Usage

To compute the StringHash value of a String, simply use the SStrHash2 helper class:

```$xslt
String result = SStrHash2.hash(input);
```

Where "input" is a String.

To break an existing StringHash, create a new StringHashBreakerThread, and then run it. When the thread finished, retrieve your result by accessing thread.getPlaintext()

```$xslt
StringHashBreakerThread thread = new StringHashBreakerThread(hash);
thread.run();
System.out.println("Result: " + thread.getPlaintext());
```

Do keep in mind that running this hash breaker could take some time. It is a brute force attack.