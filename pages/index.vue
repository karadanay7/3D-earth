<template>
  <div class="min-h-screen bg-black overflow-scroll">
    <div class="flex flex-row flex-wrap h-screen p-8 font-index z-30">
      <div
        class="text-4xl md:text-5xl lg:text-7xl text-gray-200 flex flex-col justify-center items-center lg:items-start w-full lg:w-1/2 tracking-wider gap-10 font-index no-wrap pt-10 lg:pt-0 pb-0 lg:pb-32"
      >
        <h1>3D Innovation Meets</h1>
        <h1>Full Stack Expertise!</h1>
        <div class="flex flex-col pt-8 md:pt-14 items-start">
          <div class="text-3xl">
            <NuxtLink
              target="_blank"
              to="https://www.linkedin.com/in/aysegulkaradan/"
              class="mx-4 text-gray-50 hover:text-[#2272FF]"
              alt="linkedin"
              aria-label="connect with linkedin"
            >
              <Icon name="uil:linkedin" class="text-5xl md:text-7xl" />
            </NuxtLink>
            <NuxtLink
              target="_blank"
              to="mailto:karadan.ay7@gmail.com"
              class="mx-4 text-gray-50 hover:text-[#2272FF]"
              alt="mailto"
              aria-label="connect with mail"
            >
              <Icon name="uil:envelope" class="text-5xl md:text-7xl" />
            </NuxtLink>
            <NuxtLink
              target="_blank"
              alt="github"
              to="https://github.com/karadanay7"
              class="mx-4 text-gray-50 hover:text-[#2272FF]"
              aria-label="connect with github"
            >
              <Icon name="uil:github" class="text-5xl md:text-7xl" />
            </NuxtLink>

            <h2 class="text-2xl md:text-3xl text-gray-50 text-center m-3">
              Aysegul Karadan
            </h2>
          </div>
        </div>
      </div>
      <div class="w-full lg:w-1/2 h-full">
        <iframe
          src="https://my.spline.design/3dearth-667970a2f8b6e103104b93273b2a97f3/"
          frameborder="0"
          width="100%"
          height="100%"
        ></iframe>
      </div>
    </div>
  </div>
</template>
<!-- 
<script setup>
import SplineLoader from "@splinetool/loader";
import * as THREE from "three";
import Stats from "three/addons/libs/stats.module.js";
import { OrbitControls } from "three/examples/jsm/controls/OrbitControls.js";
import { onMounted, ref } from "vue";

const threeContainer = ref(null);
let camera, scene, renderer, controls, stats;
let loadedObject;

onMounted(() => {
  const container = threeContainer.value;

  // Set up camera, scene, loader, and renderer
  camera = new THREE.OrthographicCamera(
    window.innerWidth / -2,
    window.innerWidth / 2,
    window.innerHeight / 2,
    window.innerHeight / -2,
    -50000,
    10000
  );
  camera.position.set(0, 0, 0);

  scene = new THREE.Scene();

  const loader = new SplineLoader();
  loader.load(
    "https://prod.spline.design/G01ekcHVqkSQPQET/scene.splinecode",
    (splineScene) => {
      loadedObject = splineScene;
      scene.add(loadedObject);
    }
  );

  renderer = new THREE.WebGLRenderer({ antialias: true });
  renderer.setSize(window.innerWidth, window.innerHeight);
  container.appendChild(renderer.domElement);

  renderer.shadowMap.enabled = true;
  renderer.shadowMap.type = THREE.PCFShadowMap;

  scene.background = new THREE.Color("#000000");
  renderer.setClearAlpha(0);

  // Set up controls
  controls = new OrbitControls(camera, renderer.domElement);
  controls.enableDamping = true;
  controls.dampingFactor = 0.125;

  // Set up stats
  stats = new Stats();
  stats.showPanel(0); // 0: fps, 1: ms, 2: mb, 3+: custom
  container.appendChild(stats.dom);

  // Handle window resize
  window.addEventListener("resize", onWindowResize);

  // Start the animation loop
  animate();
});

function onWindowResize() {
  camera.left = window.innerWidth / -2;
  camera.right = window.innerWidth / 2;
  camera.top = window.innerHeight / 2;
  camera.bottom = window.innerHeight / -2;
  camera.updateProjectionMatrix();
  renderer.setSize(window.innerWidth, window.innerHeight);
}

function animate() {
  requestAnimationFrame(animate);

  // Rotate the loaded object horizontally
  if (loadedObject) {
    loadedObject.rotation.y += 0.001; // Adjust the rotation speed as needed
  }

  // Update controls
  controls.update();

  // Render the scene
  renderer.render(scene, camera);

  // Update stats
  stats.update();
}
</script> -->
