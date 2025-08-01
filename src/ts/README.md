# FlatGeobuf for JavaScript / TypeScript

## Building

### Prerequisites

You must have [`pnpm`](https://pnpm.io) installed.

### Install FlatGeobuf dependencies

    pnpm install

### Build

To compile the typescript into a javascript bundle

    pnpm build

See the `scripts` section in [package.json](../../package.json) for other actions.

### Testing the examples locally.

The examples are hard coded to pull in the publicly released artifact.
If you'd like to test against your local changes, after running `pnpm build`,
update the `<script src=` tags in the examples.

For example:

```diff
diff --git a/examples/leaflet/filtered.html b/examples/leaflet/filtered.html
index 2e13dfc..da4b07e 100644
--- a/examples/leaflet/filtered.html
+++ b/examples/leaflet/filtered.html
@@ -4,7 +4,7 @@
     <link rel="stylesheet" href="/examples/site.css" />
     <script src="https://unpkg.com/underscore@1.13.6/underscore-min.js"></script>
     <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
-    <script src="https://unpkg.com/flatgeobuf@3.32.0/dist/flatgeobuf-geojson.min.js"></script>
+    <script src="/dist/flatgeobuf-geojson.min.js"></script>
     <script src="https://unpkg.com/json-formatter-js@2.5.23/dist/json-formatter.umd.js"></script>
```

You can start the built in http server with: `pnpm serve`.

Then, open the example in your browser. For example: `open http://localhost:8000/examples/leaflet/filtered.html`.
