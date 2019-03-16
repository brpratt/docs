# List of options

## F# Plugin options

### `How to set an option?`

Each option needs to be in VS Code's settings.json file. You can get to this file by going through the ***view/command pallet...*** menu, and then by typing "settings (JSON)" followed by [enter] in the revealed search box. Insert one of the settings described here into this file, in JSON syntax.

For example, plug in the last line below if you'd like an experimental speed boost:

  ...
  "workbench.statusBar.visible": false,
  "FSharp.fsacRuntime": "netcore"}

### `FSharp.fsacRuntime`

Choose the runtime of FsAutoComplete (FSAC). Require restart

**Possible values:**

* `net` - run FSAC using Full Framework (mono on non-Windows)

* `netcore` (*Experimental*) - run FSAC using .Net Core.

**Default value:** `net`

---

### `FSharp.workspaceMode`

Choose the workspace mode - way in which projects are detected in currently opened folder.

**Possible values:**

* `sln` - Tries to detecl `.sln` file in current workspace. If there are more than one `.sln` files user will be asked which one to use. If there is no `.sln` file in workspace service will fallback to `directory` mode. Search performed by FSAC using `FSharp.workspaceModePeekDeepLevel` setting.

* `directory` - Ionide loads all detected projects in the directory. Search performed by FSAC using `FSharp.workspaceModePeekDeepLevel` setting.

* `ionideSearch` - Ionide loads all detected projects in the directory. Search performed by Ionide - it was default mode pre-3.0.0 version.

**Default value:** `sln`

---

### `FSharp.workspaceModePeekDeepLevel`

Defines the depth level of directory hierarchy when searching for sln/projects

**Possible values:** `[0...99]`

**Default value:** `2`

---

### `FSharp.workspaceLoader`

Choose way the FSAC loads projects

**Possible values:**

* `projects` - loading projects is invoked by `project` request from Ionide. It's done synchronusly, one-by-one on the plugin startup. Using `ProjectCracker` for non-SDK projects, `dotnet-project-info` for SDK based projects.

* `workspaceLoad` (*Experimental*) - loading projects is triggered by `workspaceLoad` request from Ionide. Process is done asynchronusly, notifications are pushed by FSAC to Ionide through web sockets.

**Default value:** `projects`

---

### `FSharp.logLanguageServiceRequests`

Enable logging for F# Language Service requests (FSAC) to either an output channel, the developer tools console, or both

**Possible values:**

* `none` - turns off logging

* `output` - logs to output channel

* `devconsole` - logs to developer console

* `both` - logs to both output channel and developer console

**Default value:** `output`

---

### `FSharp.logLanguageServiceRequestsOutputWindowLevel`

Set the verbosity for F# Language Service Output Channel

**Possible values:**

* `DEBUG`

* `INFO`

* `WARN`

* `ERROR`

**Default value:** `INFO`

---

### `FSharp.toolsDirPath`

The directory containing the F# tools

**Possible values:** any string

**Default value:** `""`

---

### `FSharp.monoPath`

The path to Mono executable

**Possible values:** any string

**Default value:** `mono`

---

### `FSharp.fsiFilePath`

The path to the F# Interactive tool used by Ionide-FSharp. Useful for setting 64-bits FSI in some cases.

**Possible values:** any string

**Default value:** `""`

---

### `FSharp.keywordsAutocomplete`

Includes keywords in autocomplete

**Possible values:** bool

**Default value:** `true`

---

### `FSharp.externalAutocomplete`

Includes external (from unopen modules and namespaces) symbols in autocomplete. Automatically adds open statements.

**Possible values:** bool

**Default value:** `true`

---

### `FSharp.linter`

Enables integration with FSharpLinter (additional warnings and refactorings)

**Possible values:** bool

**Default value:** `true`

---

### `FSharp.unusedOpensAnalyzer`

Enables detection of unused opens, provides quick fix.

**Possible values:** bool

**Default value:** `true`

---

### `FSharp.unusedDeclarationsAnalyzer`

Enables detection of unused declarations, provides quick fix.

**Possible values:** bool

**Default value:** `true`

---

### `FSharp.simplifyNameAnalyzer`

Enables detection of symbols usages that can be simplified, provides quick fix.

**Possible values:** bool

**Default value:** `true`

---

### `FSharp.resolveNamespaces`

Enables `resolve unopened namespaces and modules` code fix.

**Possible values:** bool

**Default value:** `true`

---

### `FSharp.fsiExtraParameters`

Allows to pass extra parameters to FSI process

**Possible values:** array of strings

**Default value:** `[]`

---

### `FSharp.saveOnSendLastSelection`

Save Current file before send LastSelection to FSI

**Possible values:** bool

**Default value:** `false`

---

### `FSharp.msbuildLocation`

Use a specific version of msbuild to build this project.

**Possible values:** string

**Default value:** `""`

---

### `FSharp.msbuildAutoshow`

Automatically shows MsBuild output panel

**Possible values:** bool

**Default value:** `false`

---

### `FSharp.msbuildHost`

Use specific MSBuild host

**Possible values:**

* `.net` - uses MsBuild installed by VS or MsBuild Tools

* `.net core` - uses `dotnet msbuild`

* `ask at first use` - promts user to choose when first time needed

* `auto` - automatically choose host based on project file

**Default value:** `auto`

---

### `FSharp.enableTreeView`

Enables solution explorer. Requires restart

**Possible values:** bool

**Default value:** `true`

---

### `FSharp.codeOutline`

Enables Code Outline tree view. Requires restart

**Possible values:** bool

**Default value:** `true`

---

### `FSharp.lineLens.enabled`

Usage mode for LineLens

**Possible values:**

* `never` - never show LineLenses

* `replaceCodeLens` - show LineLenses if CodeLenses are disabled

* `always` - always show LineLenses

**Default value:** `never`

---

### `FSharp.lineLens.prefix`

The prefix displayed before the signature.

**Possible values:** string

**Default value:** `  // `

---

### `FSharp.recordStubGeneration`

Enables record stub generation.

**Possible values:** bool

**Default value:** `true`

---

## Paket Plugin options

## FAKE Plugin options
