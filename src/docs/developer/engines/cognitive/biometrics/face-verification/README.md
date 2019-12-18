# Building a Face Verification Engine

[badge/API/Yes/green]
[badge/Search/Yes/green]
[badge/UI/Yes/green]

Face verification engines can analyze human faces in media assets, and score them as to similarity with the face(s) of a specified user identity.

## Engine Manifest

<!-- TODO

All face verification engines should specify the following parameters in their build manifest:

| Parameter | Value |
| --------- | ----- |
| `TODO` | `TODO` |
| `TODO` | `TODO` |

Here is a minimal example `manifest.json` that could apply to a face verification engine:
-->

<!--TODO: Define [](manifest.example.json ':include :type=code json')-->

See the full documentation for [engine manifest standards](/developer/engines/standards/engine-manifest/) for more details.

<!-- TODO ## Engine Input -->

<!-- TODO -->

### Training and Libraries

Training for the Face Verification Engine is done by using the `enroll` mode of the engine, specified when calling the engine. The hashed faceprint of the trained identity is stored in the library, with the hash key stored in an additional database. 

*Note*: The `verify` mode of the engine retrieves the hashed faceprint from the library corresponding to the specified username, decrypts the faceprint using the hash key, and compares the decrypted faceprint to the faceprint extracted from the input image.

## Engine Output

Face verification engine output should be stored as an `object` in the [vtn-standard](/developer/engines/standards/engine-output/).
Each `object` should be of type `face`, and because each verified face always maps back to a specified user identity which corresponds to an entity in a library, each object should include the `entityId` of the entity in the library, along with the `libraryId`.

### Example

Here is an example of the simplest type of face verification engine output:

[](vtn-standard.example.json ':include :type=code json')
