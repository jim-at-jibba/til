# A testing framework to follow

When writing tests, try to follow the [Given-When-Then](https://martinfowler.com/bliki/GivenWhenThen.html) framework to help make the process of writing tests easier and faster. It also helps communicate the purpose of your tests better so it should be easier to read by your future self and others.

| State    | Explanation                                          | Code                                |
|--------- | -----------------------------------------------------| ------------------------------------|
| Given    | the state of the application before the test runs    | setup code, fixtures, database state|
| When     | the behavior/logic being tested                      | code under test                     |
| Then     | the expected changes based on the behavior           | asserts                             |



```python
def test_ping(test_app):
    # Given
    # test_app

    # When
    response = test_app.get("/ping")

    # Then
    assert response.status_code == 200
    assert response.json() == {"environment": "dev", "ping": "pong!", "testing": True}
    ```
