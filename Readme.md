# Fixture.

Package fixture provides test assertions using test fixtures with nice line diffs, and an -update flag for bootstrapping & updating fixtures.

## Example

```go
func TestGenerate(t *testing.T) {
  // ... pretend we generate some client code here for TypeScript
  var act bytes.Buffer
  err = tsclient.Generate(&act)
  assert.NoError(t, err, "generating")

  // assert the contents of act.Bytes() to the test fixture ./testdata/client.ts
  fixture.Assert(t, "client.ts", act.Bytes())
}
```

























