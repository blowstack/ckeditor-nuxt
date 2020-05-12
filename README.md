# ckeditor-nuxt

## Requirements
```
yarn add nuxt # OR npm i nuxt
```

## Component integration
```
yarn add @blowstack/ckeditor-nuxt # OR npm install --save @blowstack/ckeditor-nuxt
```

## Usage
```
<template>
........
  <client-only placeholder="loading...">
    <ckeditor-nuxt v-model="contentHolder" :config="editorConfig"  />
  </client-only>
........
</template>

<script>
export default {
    components: {
      'ckeditor-nuxt': () => import(' @blowstack/ckeditor-nuxt')
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
        }
      }
   }
}
</script>

```

