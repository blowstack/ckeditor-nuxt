# ckeditor-nuxt
CKEditor 5 editor for nuxt apps. The component includes all free available plugins (except CKFinder, instead simple upload adapter used)

## Requirements
```
yarn add nuxt
npm i nuxt
```

## Component integration
```
yarn add @blowstack/ckeditor-nuxt
npm install --save @blowstack/ckeditor-nuxt
```

## List of included plugins
* Alignment,
* AutoImage,
* Autoformat,
* Autolink,
* BlockQuote,
* Bold,
* CloudServices,
* Code,
* CodeBlock,
* Essentials,
* FontBackgroundColor,
* FontColor,
* FontFamily,
* FontSize,
* Heading,
* Highlight,
* HorizontalLine,
* Image,
* ImageCaption,
* ImageInsert,
* ImageResize,
* ImageStyle,
* ImageToolbar,
* ImageUpload,
* Indent,
* IndentBlock,
* Italic,
* Link,
* LinkImage,
* List,
* ListStyle,
* MathType,
* MediaEmbed,
* MediaEmbedToolbar,
* PageBreak,
* Paragraph,
* PasteFromOffice,
* RemoveFormat,
* SimpleUploadAdapter,
* SpecialCharacters,
* SpecialCharactersArrows,
* SpecialCharactersCurrency,
* SpecialCharactersEssentials,
* SpecialCharactersLatin,
* SpecialCharactersMathematical,
* SpecialCharactersText,
* Strikethrough,
* Subscript,
* Superscript,
* Table,
* TableCellProperties,
* TableProperties,
* TableToolbar,
* TextTransformation,
* Title,
* TodoList,
* Underline,
* WordCount

## Usage
```
<template>
  <client-only placeholder="loading...">
    <ckeditor-nuxt v-model="contentHolder" :config="editorConfig"  />
  </client-only>
</template>

<script>
export default {
  components: {
    'ckeditor-nuxt': () => { if (process.client) { return import('@blowstack/ckeditor-nuxt') } },
  },
  data() {
    return {
      editorConfig: {
        simpleUpload: {
          uploadUrl: 'path_to_image_controller',
          headers: {
            'Authorization': 'optional_token'
          }
        }
      },
      contentHolder: ""
    }
  }
}
</script>
```
## Customization

To make customization use editorConfig object.
It works the same way as the default ckeditor 5.
More info at https://ckeditor.com/docs/ckeditor5/latest/api/module_core_editor_editorconfig-EditorConfig.html

For example if you want to disable Title plugin:

```

editorConfig: {
    removePlugins: ['Title'],
}
```

You can also change the behaviour of any plugin. For the Title plugin you can change for example the placeholder:

```

editorConfig: {
    title: {
        placeholder: 'h1'
    }
}
```
