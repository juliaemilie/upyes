<script setup>
import { ref } from 'vue';

const isLTR = ref(getComputedStyle(document.body).direction === 'ltr' ? true : false);
import TextItem from '@/components/TextItem.vue';
import EmissionTable from '@/components/EmissionTable.vue';
import Sidebar from '@/components/Sidebar.vue'
</script>

<template>  
  <Sidebar :alignLeft="isLTR"></Sidebar>
  <div class="container-fluid px-2 px-sm-3 px-md-5 px-lg-0">    
    <div class="col-lg-8" :class="[isLTR ? 'offset-lg-3' : 'offset-lg-1']" id="#text-content">
      <section class="pt-4">
        <h1 class="m-3">Klimaschutz</h1>
        <figure class="text-center">
          <blockquote class="blockquote">
            <p>"Wir können eine Zukunft nicht akzeptieren, in der die Reichen in klimatisierten Blasen
              geschützt sind, während der Rest der Menschheit von tödlichem Wetter in unbewohnbaren
              Ländern heimgesucht wird." </p>
          </blockquote>
          <figcaption class="blockquote-footer">
            UN-Generalsekretär António Guterres
          </figcaption>
        </figure>
        <p class="lead">
          Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt
          ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo
          dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor
          sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor
          invidunt ut labore et dolore
        </p>
      </section>


      <TextItem id="climatecrisis">
        <template #heading>Die Klimakrise</template>
        <p>
          Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor
          invidunt
          ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo
          duo
          dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum
          dolor
          sit amet. Lorem ipsum dolor sit
        </p>
        <p>
          Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor
          invidunt
          ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo
          duo
          dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum
          dolor
          sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod
          tempor
          invidunt ut
        </p>
      </TextItem>

      <EmissionTable></EmissionTable>

      <TextItem id="projects">
        <template #heading>Unsere Projekte</template>
        <p>
          Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor
          invidunt
          ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo
          duo
          dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum
          dolor
          sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod
          tempor
          invidunt ut labore et dolore
        </p>
        <p>
          Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor
          invidunt
          ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo
          duo
          dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum
          dolor
          sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod
          tempor
          invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam
          et
          justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem
          ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam
          nonumy
          eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero
          eos
          et accusam et justo duo
        </p>
      </TextItem>

      <section class="container my-4" id="getactive">
        <div class="row">
          <h2 class="mb-3">Werde aktiv</h2>
          <div class="col-lg-4">
            <img src="@/assets/windmill.jpg" alt="Windrad" class="img-fluid">
            <h2 class="fs-4 p-3">Informiere dich</h2>
            <p>
              Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod
              tempor
              invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et
              accusam et
              justo duo dolores et ea rebum. Stet clita kasd
            </p>
          </div>
          <div class="col-lg-4">
            <img src="@/assets/demonstration.jpg" alt="Klima-Demonstration" class="img-fluid">
            <h2 class="fs-4 p-3">Engangiere dich</h2>
            <p>
              Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod
              tempor
              invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et
              accusam et
              justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea
            </p>
          </div>
          <div class="col-lg-4">
            <img src="@/assets/teamspirit.jpg" alt="Team" class="img-fluid">
            <h2 class="fs-4 p-3">Bilde ein Team</h2>
            <p>
              Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod
              tempor
              invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et
              accusam et
              justo duo dolores et ea rebum. Stet clita kasd gubergren.
            </p>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>
