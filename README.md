# github.com/speakeasy-sdks/leapml-go-sdk

<!-- Start SDK Installation -->
## SDK Installation

```bash
go get github.com/speakeasy-sdks/leapml-go-sdk
```
<!-- End SDK Installation -->

## SDK Example Usage
<!-- Start SDK Example Usage -->
```go
package main

import (
    "log"
    "github.com/speakeasy-sdks/leapml-go-sdk"
    "github.com/speakeasy-sdks/leapml-go-sdk/pkg/models/shared"
    "github.com/speakeasy-sdks/leapml-go-sdk/pkg/models/operations"
)

func main() {
    s := leapml.New()
    
    req := operations.ModelsControllerCreateRequest{
        Security: operations.ModelsControllerCreateSecurity{
            Bearer: shared.SchemeBearer{
                Authorization: "Bearer YOUR_BEARER_TOKEN_HERE",
            },
        },
        Request: shared.CreateModelDto{
            SubjectIdentifier: "unde",
            SubjectKeyword: "deserunt",
            Title: "porro",
        },
    }
    
    res, err := s.FineTuning.ModelsControllerCreate(ctx, req)
    if err != nil {
        log.Fatal(err)
    }

    if res.ModelEntity != nil {
        // handle response
    }
```
<!-- End SDK Example Usage -->

<!-- Start SDK Available Operations -->
## SDK Available Operations


### FineTuning

* `ModelsControllerCreate` - Create Model
* `ModelsControllerFindAll` - List All Models
* `ModelsControllerFindOne` - Retrieve a Single Model
* `ModelsControllerQueue` - Queue Training Job
* `SamplesControllerCreate` - Upload Image Samples
* `SamplesControllerFindAll` - List Image Samples
* `SamplesControllerFindOne` - Get Image Sample
* `SamplesControllerRemove` - Archive Image Sample
* `VersionsControllerFindAll` - List All Model Versions
* `VersionsControllerFindOne` - Get Model Version

### GeneratingImages

* `InferencesControllerCreate` - Generate Image
* `InferencesControllerFindAll` - List Inference Jobs
* `InferencesControllerFindOne` - Get Single Inference Job
* `InferencesControllerRemove` - Delete Inference

### ImageEditing

* `EditControllerCreate` - Edit a photo
* `EditControllerFindOne` - Get an edit
<!-- End SDK Available Operations -->

### SDK Generated by [Speakeasy](https://docs.speakeasyapi.dev/docs/using-speakeasy/client-sdks)
