# vue-pic-video

An easy way to capture and preview files in vue.

## Getting Started
Import the component and style it as you wish!

```
npm i --save @hazin/vue-pic-video
```

```
yarn add @hazin/vue-pic-video
```

```
import vuePicVideo from '@hazin/vue-pic-video'
```

### Example

```
<template>
  <div class="hello">
    <vue-pic-video :accept="'image/*'" @preview="previewImage" @value="captureFile">
      <button>Upload image</button>
    </vue-pic-video>
    <img :src="image" width="200px" height="200px" alt="">
    <vue-pic-video :accept="'video/*'" @preview="previewVideo" @value="captureFile">
      <button>Upload video</button>
    </vue-pic-video>
    <video :src="video" width="200px" controls></video>
  </div>
</template>
<script>
```

```
<script>
import vuePicVideo from '@hazin/vue-pic-video'

export default {
  data () {
    return {
      image: '',
      video: ''
    }
  },
  components: {
    vuePicVideo
  },
  methods: {
    previewImage (preview) { this.image = preview },
    previewVideo (preview) { this.video = preview },
    captureFile: value => { console.log(value) }
  }
}
</script>

```


## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Authors

* **Bernardo hazin** - [Hazin](https://github.com/BernardoHazin)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
