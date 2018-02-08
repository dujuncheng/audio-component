# audio-component

> this component can make it convenient to add an audio and delete an audio in a web page based by vue, which means you can play any number of audios at the same time


这是一个添加背景音乐的组件，可以方便的暂停，播放，随意添加任意数量的背景音乐，暂停所有的背景音乐，重新播放所有的背景音乐

使用比较简单，只需要引入该组件
```html
          <background-music ref="audioComponent"></background-music>

```
然后调用addMusic方法，

```javascript
    addAudio_1 () {
      this.$refs.audioComponent.addMusic({
          // 添加音频的名称
          name: 'bg',
          url: 'http://b0.hucdn.com/party/audio/bg_low.mp3',
          loop: true
      })
    },
    addAudio_2 () {
  		this.$refs.audioComponent.addMusic({
			  name: 'yao',
			  url: 'http://b0.hucdn.com/party/audio/yao_low.mp3',
			  loop: true
		  })
    },
    addAudio_3 () {
      		this.$refs.audioComponent.addMusic({
    			  name: 'over',
    			  url: 'http://b0.hucdn.com/party/audio/over_low.mp3',
    			  loop: false
    		  })
        },
    subAudio () {
	    this.$refs.audioComponent.subMusic('yao')
    }
```


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
