<template>
  <div id="projects" class="bg-light_cyan h-auto pb-16 pt-8">
    <h1 class="font-bold text-center text-4xl mb-8 tracking-widest">
      Projects
    </h1>
    <div class="flex flex-col lg:flex-row justify-center items-center">
      <div
        class="project-container max-w-xs md:max-w-full m-8 bg-white rounded overflow-hidden shadow"
      >
        <div class="project-container__image-container relative">
          <img
            class="project-container__image"
            src="~/assets/images/BISProject.jpg"
            alt=""
          />
          <div
            class="absolute left-0 top-0 bg-white transition-opacity duration-500 ease-in-out h-full p-4 opacity-0 hover:opacity-100"
          >
            <div class="flex h-full items-center">
              <p class="text-black">
                In this project, I had to use a haptic device that enables blind
                users to continuously track the absolute position of moving
                objects in virtual environments. With DualPanto I had to create
                either an application that would be helpful for the blind users
                or games that are possible to play by blind users. I created
                Super Mario using Unity Engine. It was a great experience as I
                learnt the process of creating a small game with a small group
                of intended target users (in my case, for blind users.)
              </p>
            </div>
          </div>
        </div>
        <div class="text-colar_pink font-semibold p-4 text-center">
          DualPanto Project for Blind People
        </div>
      </div>
      <div
        class="project-container max-w-xs md:max-w-full m-8 bg-white mb-8 rounded overflow-hidden shadow"
      >
        <div class="project-container__image-container relative">
          <img
            class="project-container__image"
            src="~/assets/images/DLProject.jpg"
            alt=""
          />
          <div
            class="absolute left-0 top-0 bg-white transition-opacity duration-500 ease-in-out h-full p-4 opacity-0 hover:opacity-100"
          >
            <div class="flex h-full items-center">
              <p>
                In this project, we had to build a group of five people and
                built a model, which recommends similar songs based on given
                input songs. We had to demonstrate our system by showcasing
                recommendations for various famous titles. We tried to build an
                autoencoder to get the encodings, based on which we can compare
                songs. The focus of this project was Deep Learning.
              </p>
            </div>
          </div>
        </div>
        <div class="text-colar_pink font-semibold p-4 text-center">
          Recommender System Project
        </div>
      </div>
      <div
        class="project-container max-w-xs md:max-w-full m-8 bg-white rounded overflow-hidden shadow"
      >
        <div class="project-container__image-container relative">
          <img
            src="~/assets/images/BIDProject.jpg"
            alt=""
            class="project-container__image"
          />
          <div
            class="absolute left-0 top-0 bg-white transition-opacity duration-500 ease-in-out h-full p-4 opacity-0 hover:opacity-100"
          >
            <div class="flex h-full items-center">
              <p class="text-sm md:text-base">
                This project is about building an arduino robot with light
                sensors, which can differentiate three different colors (black,
                gray, white). In this project, I learnt how motors and gears
                work and how wheels were able to turn smoothly with the minimum
                friction. The objective of this project was, to place the on the
                on the black, white and gray patterned circle map, then identify
                the center of the circle and stop exactly on the circle spot. I
                had a lot of fun building a robot by myself with arduino and
                even had a chance to design my own robot using a 3D printer and
                a laser cutter.
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
