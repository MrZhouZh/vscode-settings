<samp><b>Jace's VSCode settings</b></samp>

[`.vscode/settings.json`](./.vscode/settings.json)<br />
{
	// Place your global snippets here. Each snippet is defined under a snippet name and has a scope, prefix, body and 
	// description. Add comma separated ids of the languages where the snippet is applicable in the scope field. If scope 
	// is left empty or omitted, the snippet gets applied to all languages. The prefix is what is 
	// used to trigger the snippet and the body will be expanded and inserted. Possible variables are: 
	// $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders. 
	// Placeholders with the same ids are connected.
	// Example:
	// "Print to console": {
	// 	"scope": "javascript,typescript",
	// 	"prefix": "log",
	// 	"body": [
	// 		"console.log('$1');",
	// 		"$2"
	// 	],
	// 	"description": "Log output to console"
	// }
	"import": {
    "scope": "javascript,typescript",
    "prefix": "im",
    "body": [
      "import { $1 } from '$2';"
    ],
    "description": "Import a module"
  },
  "export-all": {
    "scope": "javascript,typescript",
    "prefix": "ex",
    "body": [
      "export * from '$2';"
    ],
    "description": "Export a module"
  },
  "vue-script-setup": {
    "scope": "vue",
    "prefix": "<sc",
    "body": [
      "<script setup lang=\"ts\">",
      "const props = defineProps<{",
      "  modelValue?: boolean,",
      "}>()",
      "$1",
      "</script>",
      "",
      "<template>",
      "  <div>",
      "    <slot/>",
      "  </div>",
      "</template>",
    ]
  },
  "vue-template-ref": {
    "scope": "javascript,typescript,vue",
    "prefix": "tref",
    "body": [
      "const ${1:el} = shallowRef<HTMLDivElement>()",
    ]
  },
  "vue-computed": {
    "scope": "javascript,typescript,vue",
    "prefix": "com",
    "body": [
      "computed(() => { $1 })"
    ]
  },
  "vue-watch-effect": {
    "scope": "javascript,typescript,vue",
    "prefix": "watchE",
    "body": [
      "watchEffect(() => {",
      "  $1",
      "})"
    ]
  },
  "if-vitest": {
    "scope": "javascript,typescript",
    "prefix": "ifv",
    "body": [
      "if (import.meta.vitest) {",
      "  const { describe, it, expect } = import.meta.vitest",
      "  ${1}",
      "}"
    ]
  },
  "markdown-api-table": {
    "scope": "markdown",
    "prefix": "table",
    "body": [
      "<table>",
      "<tr>",
      "<td width=\"400px\" valign=\"top\">",
      "",
      "### API",
      "",
      "Description",
      "",
      "</td>",
      "<td width=\"600px\"><br>",
      "",
      "```ts",
      "// code block",
      "```",
      "",
      "</td>",
      "</tr>",
      "</table>",
    ],
  }
}

