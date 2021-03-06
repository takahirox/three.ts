# Goals

* Inline JSDoc comments on most functions, variables.
* Utilize the typing from Typscript to generate rich documentation.

## Naming Convention

### Transform Matrix Names

* All matrices should be named in the form: [x]To[Y], where x is the originating space, and the y is the space after applying this matrix.
* If you invert a [x]To[Y] matrix, it should now be called [y]To[X].

Examples:

```
let worldToLocal = new Matrix4();
let localToWorld = worldToLocal.clone.invert();

let localToScreenProjection = new Matrix4().makePerspectiveProjection( 1.0, 1.0, 1000.0, 1.0 );
let screenToLocalUnprojection = localToScreenProjection.clone().invert();
```
