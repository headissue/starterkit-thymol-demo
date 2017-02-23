![license](https://img.shields.io/github/license/headissue/starterkit-thymol-demo.svg)

Demo StarterKit for Thymol
==========================

The Demo StarterKit for Thymol is meant to show off some of the capabilities of developing Thmyol/Thymeleaf-based projects in Pattern Lab.

Requirements
------------

- The node version of Pattern Lab (this StarterKit does not work with the PHP version)
- Either the [Gulp Edition](https://github.com/pattern-lab/edition-node-gulp) or [Grunt Edition](https://github.com/pattern-lab/edition-node-grunt) for Pattern Lab

#### Setting up the PatternEngine
The Demo StarterKit for Thmyol requires the following PatternEngine:

-	`headissue/patternengine-node-thmyol`: [GitHub](https://github.com/headissue/patternengine-node-thmyol), [npm](https://www.npmjs.com/package/patternengine-node-thymol)

#### Configuring Pattern Lab to use Thymol templates
Editions are shipped with a default configuration for Mustache.
Therefor, the following changes must be made to `patternlab-config.json`:

- Change 
  ```json
  "patternExtension": "mustache"
  ```
  to 
  ```json
  "patternExtension": "html"
  ```

- For faster development, enable [Incremental Builds](https://github.com/pattern-lab/patternlab-node/wiki/Incremental-Builds):
  
  ```json
  "cleanPublic": true
  ```

## 
Install
-------

Modify `package.json` to add the `Thymol` engine and this StarterKit to the `dependencies` section:

```json
"dependencies": {
  "patternengine-node-thymol": "^0.1.1",
  "starterkit-thymol-demo": "^1.0.0"
  ...
}
```

and run
```bash
npm install
```
to automatically install the Thymol PatternEngine and the StarterKit.

#### Manual installation

Then this StarterKit can be installed via one of the following commands:

- **Gulp edition**
	
	```bash
	gulp patternlab:loadstarterkit --kit=starterkit-thymol-demo --clean=true  
	```

- **Grunt edition**

	<p>See <em>Known issues</em> below!</p>
	
	```bash
	grunt patternlab:loadstarterkit --kit=starterkit-thymol-demo --clean=true  
	```

## Known issues
**_Grunt_ edition**: As of 23rd March, 2017, no files are copied. See [Loading starterkit does not copy files](https://github.com/pattern-lab/edition-node-grunt/issues/12) for details. As
 a workaround:
 
 1. Delete everything under `source`
 2. Download the latest release of [this StarterKit on GitHub](https://github.com/headissue/starterkit-thymol-demo) and copy the contents of `dist` into the `source` folder

Edit Files
----------

After installation the files for this StarterKit can be found in `source/`.

Acknowledgements
----------------
This repository is based on the [Demo StarterKit for Mustache](https://github.com/pattern-lab/starterkit-mustache-demo) by Brad Frost and Dave Olsen
