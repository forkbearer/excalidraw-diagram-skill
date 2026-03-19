# Element Templates

Copy-paste JSON templates for each Excalidraw element type. The `strokeColor` and `backgroundColor` values are placeholders — always pull actual colors from `color-palette.md` based on the element's semantic purpose.

## Free-Floating Text (no container)
```json
{
  "type": "text",
  "id": "label1",
  "x": 100, "y": 100,
  "width": 200, "height": 25,
  "text": "Section Title",
  "originalText": "Section Title",
  "fontSize": 20,
  "fontFamily": 3,
  "textAlign": "left",
  "verticalAlign": "top",
  "strokeColor": "<title color from palette>",
  "backgroundColor": "transparent",
  "fillStyle": "solid",
  "strokeWidth": 1,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 11111,
  "version": 1,
  "versionNonce": 22222,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": null,
  "link": null,
  "locked": false,
  "containerId": null,
  "lineHeight": 1.25
}
```

## Line (structural, not arrow)
```json
{
  "type": "line",
  "id": "line1",
  "x": 100, "y": 100,
  "width": 0, "height": 200,
  "strokeColor": "<structural line color from palette>",
  "backgroundColor": "transparent",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 44444,
  "version": 1,
  "versionNonce": 55555,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": null,
  "link": null,
  "locked": false,
  "points": [[0, 0], [0, 200]]
}
```

## Small Marker Dot
```json
{
  "type": "ellipse",
  "id": "dot1",
  "x": 94, "y": 94,
  "width": 12, "height": 12,
  "strokeColor": "<marker dot color from palette>",
  "backgroundColor": "<marker dot color from palette>",
  "fillStyle": "solid",
  "strokeWidth": 1,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 66666,
  "version": 1,
  "versionNonce": 77777,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": null,
  "link": null,
  "locked": false
}
```

## Ellipse (Circle) with Text Inside
Use this when an ellipse/circle needs a label centered inside it. The ellipse must declare `boundElements` and the text must set `containerId`.
```json
{
  "type": "ellipse",
  "id": "circle1",
  "x": 100, "y": 100, "width": 120, "height": 120,
  "strokeColor": "<stroke from palette based on semantic purpose>",
  "backgroundColor": "<fill from palette based on semantic purpose>",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 66666,
  "version": 1,
  "versionNonce": 77777,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": [{"id": "circle_text1", "type": "text"}],
  "link": null,
  "locked": false
}
```
```json
{
  "type": "text",
  "id": "circle_text1",
  "x": 100, "y": 148,
  "width": 120, "height": 25,
  "text": "Label",
  "originalText": "Label",
  "fontSize": 16,
  "fontFamily": 3,
  "textAlign": "center",
  "verticalAlign": "middle",
  "strokeColor": "<text color from palette>",
  "backgroundColor": "transparent",
  "fillStyle": "solid",
  "strokeWidth": 1,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 88888,
  "version": 1,
  "versionNonce": 99999,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": null,
  "link": null,
  "locked": false,
  "containerId": "circle1",
  "lineHeight": 1.25
}
```

## Rectangle
```json
{
  "type": "rectangle",
  "id": "elem1",
  "x": 100, "y": 100, "width": 180, "height": 90,
  "strokeColor": "<stroke from palette based on semantic purpose>",
  "backgroundColor": "<fill from palette based on semantic purpose>",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 12345,
  "version": 1,
  "versionNonce": 67890,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": [{"id": "text1", "type": "text"}],
  "link": null,
  "locked": false,
  "roundness": {"type": 3}
}
```

## Text (centered in shape)
Font size should match the hierarchy tier: 36px (title), 20px (primary component label), 16px (secondary label), 14px (annotation/detail). Never go below 14px.
```json
{
  "type": "text",
  "id": "text1",
  "x": 130, "y": 132,
  "width": 120, "height": 25,
  "text": "Process",
  "originalText": "Process",
  "fontSize": 16,
  "fontFamily": 3,
  "textAlign": "center",
  "verticalAlign": "middle",
  "strokeColor": "<text color — match parent shape's stroke or use 'on light/dark fills' from palette>",
  "backgroundColor": "transparent",
  "fillStyle": "solid",
  "strokeWidth": 1,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 11111,
  "version": 1,
  "versionNonce": 22222,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": null,
  "link": null,
  "locked": false,
  "containerId": "elem1",
  "lineHeight": 1.25
}
```

## Arrow
```json
{
  "type": "arrow",
  "id": "arrow1",
  "x": 282, "y": 145, "width": 118, "height": 0,
  "strokeColor": "<arrow color — typically matches source element's stroke from palette>",
  "backgroundColor": "transparent",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 33333,
  "version": 1,
  "versionNonce": 44444,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": null,
  "link": null,
  "locked": false,
  "points": [[0, 0], [118, 0]],
  "startBinding": {"elementId": "elem1", "focus": 0, "gap": 2},
  "endBinding": {"elementId": "elem2", "focus": 0, "gap": 2},
  "startArrowhead": null,
  "endArrowhead": "arrow"
}
```

For curves: use 3+ points in `points` array.

---

## Architecture Element Templates

Standard building blocks for system design and software architecture diagrams. All sizes follow the 8-point grid. Pull colors from `color-palette.md` based on semantic purpose.

### Service / Microservice (160×72)
```json
{
  "type": "rectangle",
  "id": "service1",
  "x": 100, "y": 100, "width": 160, "height": 72,
  "strokeColor": "<stroke from palette>",
  "backgroundColor": "<fill from palette>",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 110001,
  "version": 1,
  "versionNonce": 110002,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": [{"id": "service1_label", "type": "text"}],
  "link": null,
  "locked": false,
  "roundness": {"type": 3}
}
```

### External System (160×80, dashed stroke)
Use for any system outside your ownership boundary. Dashed stroke signals "external".
```json
{
  "type": "rectangle",
  "id": "ext1",
  "x": 100, "y": 100, "width": 160, "height": 80,
  "strokeColor": "<stroke from palette — use Inactive/Disabled>",
  "backgroundColor": "<fill from palette — use Inactive/Disabled>",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "dashed",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 120001,
  "version": 1,
  "versionNonce": 120002,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": [{"id": "ext1_label", "type": "text"}],
  "link": null,
  "locked": false,
  "roundness": {"type": 3}
}
```

### Database / Data Store (160×80, cylinder hint)
Excalidraw has no native cylinder. Approximate it: rectangle with a narrow ellipse on top to suggest a cylinder cap.
```json
{
  "type": "rectangle",
  "id": "db1",
  "x": 100, "y": 116, "width": 160, "height": 64,
  "strokeColor": "<stroke from palette>",
  "backgroundColor": "<fill from palette>",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 130001,
  "version": 1,
  "versionNonce": 130002,
  "isDeleted": false,
  "groupIds": ["db1_group"],
  "boundElements": [{"id": "db1_label", "type": "text"}],
  "link": null,
  "locked": false
}
```
```json
{
  "type": "ellipse",
  "id": "db1_cap",
  "x": 100, "y": 100, "width": 160, "height": 32,
  "strokeColor": "<same stroke as rectangle>",
  "backgroundColor": "<same fill as rectangle>",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 130003,
  "version": 1,
  "versionNonce": 130004,
  "isDeleted": false,
  "groupIds": ["db1_group"],
  "boundElements": null,
  "link": null,
  "locked": false
}
```

### Message Queue / Event Bus (200×64, wider and thinner)
Width signals a channel/bus; thinner height distinguishes it from a service.
```json
{
  "type": "rectangle",
  "id": "queue1",
  "x": 100, "y": 100, "width": 200, "height": 64,
  "strokeColor": "<stroke from palette>",
  "backgroundColor": "<fill from palette>",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 140001,
  "version": 1,
  "versionNonce": 140002,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": [{"id": "queue1_label", "type": "text"}],
  "link": null,
  "locked": false,
  "roundness": {"type": 3}
}
```

### User / Client (80×80 ellipse)
```json
{
  "type": "ellipse",
  "id": "user1",
  "x": 100, "y": 100, "width": 80, "height": 80,
  "strokeColor": "<stroke from palette — use Start/Trigger>",
  "backgroundColor": "<fill from palette — use Start/Trigger>",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 150001,
  "version": 1,
  "versionNonce": 150002,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": [{"id": "user1_label", "type": "text"}],
  "link": null,
  "locked": false
}
```

### Zone / Swimlane Container
A large background rectangle that groups related services. Use a very light fill and no visible stroke (or a very subtle one). Place section heading as free-floating text above it.
```json
{
  "type": "rectangle",
  "id": "zone1",
  "x": 80, "y": 80, "width": 600, "height": 320,
  "strokeColor": "<subtle stroke — e.g. Inactive/Disabled stroke>",
  "backgroundColor": "<very light fill — e.g. Secondary or Tertiary fill>",
  "fillStyle": "solid",
  "strokeWidth": 1,
  "strokeStyle": "solid",
  "roughness": 0,
  "opacity": 100,
  "angle": 0,
  "seed": 160001,
  "version": 1,
  "versionNonce": 160002,
  "isDeleted": false,
  "groupIds": [],
  "boundElements": null,
  "link": null,
  "locked": false,
  "roundness": {"type": 3}
}
```
