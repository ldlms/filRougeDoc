<template>
<template>
  <div class="scrollable-container">
    <div class="scrollable" ref="scrollable">
      <div class="content">
        <img src="image1.jpg" alt="Image 1">
        <img src="image2.jpg" alt="Image 2">
        <img src="image3.jpg" alt="Image 3">
        <img src="image4.jpg" alt="Image 4">
        <img src="image5.jpg" alt="Image 5">
        <img src="image6.jpg" alt="Image 6">
      </div>
    </div>
    <button class="scroll-btn prev-btn" @click="scrollLeft"><span>&lt;</span></button>
    <button class="scroll-btn next-btn" @click="scrollRight"><span>&gt;</span></button>
  </div>
</template>

</template>



<script>
export default{
methods: {
  scrollLeft() {
    const scrollable = this.$refs.scrollable;
    scrollable.scrollLeft -= 200;
  },
  scrollRight() {
    const scrollable = this.$refs.scrollable;
    scrollable.scrollLeft += 200;
  }
}
}
</script>


<style>
.scrollable-container {
  position: relative;
  width: 100%;
  height: 400px;
  overflow: hidden;
}

.scrollable {
  display: flex;
  flex-wrap: nowrap;
  width: max-content;
  height: 100%;
  padding: 10px;
  margin-right: 70px;
}

.content {
  display: flex;
  flex-wrap: nowrap;
  width: fit-content;
  height: 100%;
}

.scrollable img {
  width: 400px;
  height: 400px;
  margin-right: 20px;
}

.scroll-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 50px;
  height: 50px;
  border-radius: 50%;
  border: none;
  background-color: rgba(255, 255, 255, 0.5);
  opacity: 0;
  transition: opacity 0.2s ease-in-out;
}

.scroll-btn span {
  display: inline-block;
  font-size: 30px;
  line-height: 1;
}

.scroll-btn:hover {
  opacity: 1;
}

.prev-btn {
  left: 0;
}

.next-btn {
  right: 0;
}
</style>