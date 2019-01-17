# p419vocab
Vocabulary work on time for Project 418 follow on work (P419)

This repository houses any temporal-related schema.org extensions.

The JSON-LD Context is served at: http://schema.geolink.org/schemaorg/time/jsonldcontext.json

## Extensions

### 1. [OWL Time](http://www.w3.org/2006/time#)

[http://www.w3.org/2006/time#](http://www.w3.org/2006/time#)

Extend [schema:temporalCoverage](https://schema.org/temporalCoverage) to allow for any OWL Time representation.

### How to markup your JSON-LD

```
{
  "@context": [
    {
      "@vocab": "http://schema.org/",
      "time": "http://www.w3.org/2006/time#"
    }, 
    "http://schema.geolink.org/schemaorg/time/jsonldcontext.json"
  ],
  "@type": "Dataset",
  "temporalConverage": {
    "@type": "time:TemporalEntity",
    "time:hasBeginning": {
      "@type": "time:Instant",
      "time:inXSDDateTimeStamp": "2015-11-01T17:58:16.102Z"
    }
  }
}
```

1. Make your `@context` an *array*.
2. Make sure the *first* context is schema.org
3. Add the temporal converage context file to the `@context`.
4. Now you can begin to use OWL Time classes as a valid `schema:temporalCoverage`


