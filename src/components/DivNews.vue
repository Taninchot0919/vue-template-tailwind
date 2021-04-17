<template>
  <div class="bg-red-200">
    <div class="h-screen">
      <div class="bg-green-200 h-2/6 min-h-0 w-11/12 mx-auto mt-10 p-5">
        <img
          src="https://images.unsplash.com/photo-1618562289507-ca85d897a5c3?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80"
          alt=""
          class="h-full rounded-lg float-left mx-10"
        />
        <div id="text" class="inline text-left ml-44">
          <h1 class="text-2xl mb-4">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia,
            molestiae.
          </h1>
          <!-- :class="test ? 'text-red-500' : 'text-white' หมายความว่า ถ้า test เป็น true ให้ทำตัวอักษรเป็นสีแดง ถ้าไม่จริงให้ทำตัวหนังสือเป็นสีขาว  -->
          <p class="mr-56" :class="test ? 'text-red-500' : 'text-white'">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem sit
            repellendus blanditiis voluptatibus soluta architecto praesentium
            cumque culpa enim similique odio nemo, quibusdam, voluptas quos
            aliquid cupiditate. Iure voluptatem cum, a odit suscipit sequi
            sapiente quis iusto laudantium fuga officiis explicabo corporis ut
            placeat vel quas. Qui repellendus dicta eaque?
          </p>
        </div>
      </div>
      <div
        class="bg-green-200 h-2/6 min-h-0 w-11/12 mx-auto mt-10 p-5"
        v-for="gallery in galleries"
        :key="gallery.id"
      >
        <img
          :src="gallery.image"
          alt=""
          class="h-full rounded-lg mx-10"
          :class="gallery.id % 2 ? 'float-left' : 'float-right'"
        />
        <div id="text" class="inline text-left ml-44" :class="gallery.id % 2 ? 'text-left' : 'text-right'">
          <h1 class="text-2xl mb-4">
            {{ gallery.title }}
          </h1>
          <!-- :class="test ? 'text-red-500' : 'text-white' หมายความว่า ถ้า test เป็น true ให้ทำตัวอักษรเป็นสีแดง ถ้าไม่จริงให้ทำตัวหนังสือเป็นสีขาว  -->
          <p class="mr-56" :class="test ? 'text-red-500' : 'text-white'">
            {{ gallery.content }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      test: true,
      galleries: [
        {
          id: 1,
          title: "El Teide Volcano, Spain",
          content: "Photo by Max Rive",
          image:
            "https://images.unsplash.com/photo-1509840841025-9088ba78a826?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80",
        },
        {
          id: 2,
          title: "El Teide Volcano, Spain",
          content: "Photo by Max Rive",
          image:
            "https://images.unsplash.com/photo-1468183654773-77e2f0bb6bf9?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80",
        },
      ],
    };
  },
};
</script>