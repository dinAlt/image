---
title: Providers
description: ''
position: 5
category: Guide
---

Complete list of internal providers.

## `local`

Local provider is an integration of ipx and image module. Local provider is an specific provider that uses for development, optimizing in-project.  
By default local provider looks `static` dir to find original images, You can change `dir` inside `nuxt.config`.
The local provider has a caching stategy to clear cached images to reduce massive disk usages. You can schedule the cache cleaning job using `clearCache` option in provide options. By default this cron job is disabled.

```js{}[nuxt.config.js]
export default {
  image: {
    providers: {
      local: {
        /**
         * Public domain of your website 
         **/
        baseURL: 'https://awesome.com/',
        /**
         * Internal address of your website 
         **/
        internalBaseURL: 'http://192.168.1.100:3000/',
        /**
         * Input directory for images
         **/
        dir: '~/static',
        /**
         * Enable/Disabel cache cleaning cron job
         **/
        clearCache: false
      }
    }
  }
}
```

## `cloudinary`

Integration between [Cloudinary](https://cloudinary.com) and the image module.  
To use this provider you just need to specify the base url of your project in cloudinary.

```js{}[nuxt.config.js]
export default {
  image: {
    providers: {
      cloudinary: {
        baseURL: 'https://res.cloudinary.com/nuxt/image/upload/'
      }
    }
  }
}
```

## `twicpics`

Integration between [Twicpics](https://www.twicpics.com) and the image module.  
To use this provider you just need to specify the base url of your project in Twicpics.

```js{}[nuxt.config.js]
export default {
  image: {
    providers: {
      twicpics: {
        baseURL: 'https://i5acur1u.twic.pics'
      }
    }
  }
}
```

## `fastly`

Integration between [Fastly](https://docs.fastly.com/en/guides/image-optimization-api)
and the image module. To use this provider you just need to specify the base url
of your service in Fastly.

```js{}[nuxt.config.js]
export default {
  image: {
    providers: {
      fastly: {
        baseURL: 'https://www.fastly.io'
      }
    }
  }
}
```

## `imgix`

Integration between [imgix](https://docs.imgix.com/) and the image module. To use this provider you just need to specify the base url of your service in imgix.

```js{}[nuxt.config.js]
export default {
  image: {
    providers: {
      imgix: {
        baseURL: 'https://assets.imgix.net'
      }
    }
  }
}
```
