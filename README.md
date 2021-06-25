# Image Finder

## Brief
We would like to build a server which allows others to find images by a search term

### Acceptance criteria 
- Ability to fetch data from an external image searching API
- Transform and filter the data
- Create an endpoint to allow retrieval of the transformed data

### What's next?
This is entirely up to you show us how you would take this.


### What you need to know

For the purpose of this exercise, the external API will be NASA's media searching API

    https://images-api.nasa.gov/search?q=moon

Here is an example of the payload:

```
{
  "collection": {
    "href": "https://images-api.nasa.gov/search?q=moon",
    "version": "1.0",
    "items": [
      {
        "href": "https://images-assets.nasa.gov/image/PIA12235/collection.json",
        "data": [ ... ],
        "links": [
          {
            "href": "https://images-assets.nasa.gov/image/PIA12235/PIA12235~thumb.jpg",
            "render": "image",
            "rel": "preview"
          }
        ]
      }
    ]
  }
}
```

### Expected result
Here is what we expect our service to return:

```
[
  "https://images-assets.nasa.gov/image/PIA12235/PIA12235~thumb.jpg",
  "https://images-assets.nasa.gov/image/PIA13517/PIA13517~thumb.jpg",
  ...
]
```

### Notes
- Feel free to use your local environment or codesandbox
- Please use the tools you are used i.e. the internet
