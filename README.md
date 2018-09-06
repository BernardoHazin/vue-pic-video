# vue-pic-video

An easy way to capture and preview files in vue.

## Getting Started
Import the component and style it as you wish!

```
import vuePicVideo from '@hazin/vue-pic-video'

```

### Example

```
<template>
  <div class="hello">    
    <vue-pic-video :accept="'image/*, video/*'" @preview="previewImage" @value="captureFile">
      <button>Upload file</button>
    </vue-pic-video>
  </div>
</template>
```

```
<script>
import vuePicVideo from '@hazin/vue-pic-video'

export default {
  name: 'app',
  data () {
    return {
      previewImage: ''
    }
  },
  components: {
    vuePicVideo
  },
  methods: {
    previewImage: preview => this.previewImage = preview,
    captureFile: value => console.log(value)
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
