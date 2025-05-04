<template>
  <section class="py-8 md:py-16">
    <AnimatedText :animationDelay="1" type="blur">
      <div class="container mx-auto px-4">
        <div
          class="max-w-4xl mx-auto overflow-hidden rounded-xl shadow-2xl relative cursor-pointer"
        >
          <div class="aspect-w-16 aspect-h-9 bg-gray-800 relative">
            <video poster="/img/video_thumbnail.png" controls width="250">
              <source src="/header_video.mp4" type="video/mp4" />

              <a href="/header_video.mp4">MP4</a>
              video.
            </video>
          </div>
        </div>
      </div>
    </AnimatedText>
  </section>
</template>

<style scoped>
.aspect-w-16 {
  position: relative;
  padding-bottom: 56.25%;
}
.aspect-w-16 > * {
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
</style>
