# 🐣 Baby Steps

I hate introductions. Let's have an example, and then we will start coding.

Let's say you've started a new **channel** on YouTube. Now what? Exactly. Create **videos** for your **audience**.

The words that are bolded in the previous sentence define what ReactiveX is.

In a nutshell, a source (YouTube channel) that's able to provide data (videos) for multiple recipients (audience).

So, anyone can easily **subscribe** to your channel, and watch your latest videos by:
- *Manually* checking their newsfeed (pulling)
- Receiving a notification (pushing)

Let's see how this API will look like before implementing it.

```js
// Create a YouTube channel.
const channel = new Channel()

// A subscriber will subscribe to our channel, and will provide us
// with a callback function that describes the processing of any
// new video.
const subscriber = channel.subscribe(function (video) {
  console.log(`I received a video.`)
  console.log(`The video's title is: ${video}`)
})

// Let's post a new video.
channel.publish('How To Eat A Pineapple Pizza')

// $ > I received a video.
// $ > The video's title is: How To Eat A Pineapple Pizza
```
