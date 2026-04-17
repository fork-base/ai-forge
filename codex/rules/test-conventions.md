# Test Conventions

- [TC1] No unit tests. Only module-level integration tests. Test coverage is to be achieved through extensive integration tests not unit tests. The trigger to write a test should be testing requirements of user stories. Specifically not to test implementation details.
- [TC2] When comparing floating point values in test assertions use this pattern: `(expected - actual).abs() < 1e-10`.
- [TC3] Never make anything public to test it.
- [TC4] Avoid mocks wherever possible. Use development APIs and environments instead.
- [TC5] All assertions need helpful output messages for their failure cases.
- [TC6] Tests have the structure `Expect-Execute-Assert`. This means:
 - First input data and expected values are created at the start of the test function.
 - Next the function under test is executed.
 - Last actual return values of the funcion under test are compared to the expected values.
- [TC7] Expected values are always immutable, and constructed before the function under test is run.
- [TC8] Assertions need to test exact values (e.g. >0.0 is not sufficient).
- [TC9] Expected values are not computed inside the test function. They are computed outside the code and only their values are stored as expected constants. This is to avoid mistakes in calculation or running the risk of testing implementation details.
