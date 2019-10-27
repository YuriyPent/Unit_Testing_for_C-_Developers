# Unit_Testing_for_C#_Developers
### Unit Testing for C# Developers

1. NuGet package console => TestNinjaUnitTests => Install-package NUnit -Version 3.8.1

2. NuGet package console => TestNinjaUnitTests => Install-Package NUnit3TestAdapter -Version 3.8.0

3. Add attribute [TestFixture] for class ReservationTests and [Test] for tests

4. Add using NUnit.Framework

5. Live template

   ```c#
   [Test]
   public void $Method$_$Scenario$_$Expected$()
   {
   }
   ```

### Creating Unit Tests

Tests in xUnit are defined as methods to which the **Fact** and **Theory** attributes apply. **The** Fact attribute indicates what methods the test represents.
Each method contains three logical parts - **Arrange**, **Act** and **Assert**.
The Arrange section initializes the test context.

Further, in the Act section, it performs the action itself, which needs to be tested, namely the generation of the view.
To check the result of the text in the Assert section, one of the methods of the Assert class is called.
The Arrange-Act-Assert test model represents a whole testing paradigm that is used by many unit test frameworks:

- Arrange: sets the initial conditions for the test

- Act: performs a test (usually represents a single line of code)

- Assert: Verifies the test result.

The Arrange and Act sections represent regular C # code. And the Assert section uses the class of the same name Assert, which is defined in the xUnit.net library.

To check the result, a number of methods are defined in the Assert class, among which are the following:

1. **All** (collection, action): the method confirms that all elements of the collection collection correspond to the action
2. **Contains** (expectedSubString, actualString): the method confirms that the string actualString contains the expectedSubString
3. **DoesNotContain** (expectedSubString, actualString): the method confirms that the actualString does not contain the expectedSubString
4. **DoesNotMatch** (expectedRegexPattern, actualString): the method confirms that the string actualString does not match the regular expression expectedRegexPattern
5. **Matches** (expectedRegexPattern, actualString): the method confirms that the string actualString matches the regular expression expectedRegexPattern
6. **Equal** (expected, result): the method compares the test result in the form of the result value and the expected value expected and confirms their equality
7. **NotEqual** (expected, result): the method compares the test result as the result value and the expected value expected and confirms their inequality
8. **Empty** (collection): method confirms that collection is empty
9. **NotEmpty** (collection): method confirms that collection is not empty
10. **True** (result): the method confirms that the test result is true
11. **False** (result): the method confirms that the test result is false
12. **IsType** (expected, result): the method confirms that the test result is of type expected
13. **IsNotType** (expected, result): the method confirms that the test result does not represent the expected type
14. **IsNull** (result): the method confirms that the test result is null
15. **IsNotNull** (result): the method confirms that the test result is not null
16. **InRange** (result, low, high): the method confirms that the test result is in the range between low and high
17. **NotInRange** (result, low, high): the method confirms that the test result does not belong to the range from low to high
18. **Same** (expected, actual): the method confirms that the expected and actual links point to the same object in memory
19. **NotSame** (expected, actual): the method confirms that the expected and actual links point to different objects in memory
20. **Throws** (exception, expression): the method confirms that expression throws an exception exception