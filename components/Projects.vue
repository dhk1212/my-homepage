<template>
  <div class="bg-light_cyan h-auto pb-16 pt-8">
    <h1 class="font-bold text-center text-4xl mb-8 tracking-widest">
      Projects
    </h1>
    <div class="flex flex-row justify-center">
      <div
        class="project-container m-8 bg-white rounded overflow-hidden shadow"
      >
        <div class="project-container__image-container relative">
          <img
            class="project-container__image"
            src="@/assets/images/BISProject.jpg"
            alt=""
          />
          <div
            class="absolute left-0 top-0 bg-white transition-opacity duration-500 ease-in-out h-full p-4 opacity-0 hover:opacity-100"
          >
            <div class="flex h-full items-center">
              <p class="text-black">
                In this project, I had to use a haptic device that enables blind
                users to continously track the absolute position of moving
                objects in spatial virtual environments. With DualPanto I had to
                create either an application that would be helpful for the blind
                users or games that is possible to play by blind users. I
                created Super Mario using Unity Engine. It was a great
                experience, because I learnt the process of building a small
                game targeting for a small group of users(in my case for blind
                users.)
              </p>
            </div>
          </div>
        </div>
        <div class="text-colar_pink font-semibold p-4 text-center">
          DualPanto Project for Blind People
        </div>
      </div>
      <div
        class="project-container m-8 bg-white mb-8 rounded overflow-hidden shadow"
      >
        <div class="project-container__image-container relative">
          <img
            class="project-container__image"
            src="@/assets/images/DLProject.jpg"
            alt=""
          />
          <div
            class="absolute left-0 top-0 bg-white transition-opacity duration-500 ease-in-out h-full p-4 opacity-0 hover:opacity-100"
          >
            <div class="flex h-full items-center">
              <p>
                In this project, we had to build a group of five people and
                built a model, which recommends similar songs based on a given
                input songs. We had to demonstrate our system by showcasing
                recommendations for various famous titles. We tried to an
                autoencoder to get the encodings, based on which we can compare
                songs. Most focus of this project was Deep Learning.
              </p>
            </div>
          </div>
        </div>
        <div class="text-colar_pink font-semibold p-4 text-center">
          Recommender System Project
        </div>
      </div>
      <div
        class="project-container m-8 bg-white rounded overflow-hidden shadow"
      >
        <div class="project-container__image-container relative">
          <img
            src="@/assets/images/BIDProject.JPG"
            alt=""
            class="project-container__image"
          />
          <div
            class="absolute left-0 top-0 bg-white transition-opacity duration-500 ease-in-out h-full p-4 opacity-0 hover:opacity-100"
          >
            <div class="flex h-full items-center">
              <p>
                This project is about building an arduino robot with light
                sensonrs, which had to differenciate three different
                colors(black, gray, white). In this project, I learnt how motors
                and gears work and how wheels can smoothly turn with less
                friction. The goal of this project was, the arduino robot would
                be placed on the black, white and gray pattern circle map and
                had to find the middle of the circle and had to stop exact on
                the circle spot. I had a lot of fun building a robot myself with
                arduino and even had a chance to design my own robot using 3D
                printer and laser cutter.
              </p>
            </div>
          </div>
        </div>
        <div class="text-colar_pink font-semibold p-4 text-center">
          Arduino Project with light sensors
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.project-container {
  height: 400px;
  width: 400px;
}

.project-container__image-container {
  height: 340px;
  width: 100%;
}

.project-container__image {
  height: 100%;
  width: 100%;
}
</style>
