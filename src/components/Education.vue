<script setup>
  import educ from "../assets/ansiedad.png";
  import { Calendar, GraduationCap } from "@lucide/vue";

  const educationData = [
    {
      id: "Lorem ipsum dolor",
      degree: "asdasdasd",
      institution: "consectectur adipicin elit asd.",
      duration: "2019-2023",
      details: "asdasdas rqro  oqro kdkfskd  qeo rqwrka kq.",
    },
    {
      id: "Lorem ipsum dolor",
      degree: "asdasdasd",
      institution: "consectectur adipicin elit asd.",
      duration: "2019-2023",
      details: "asdasdas rqro  oqro kdkfskd  qeo rqwrka kq.",
    },
    {
      id: "Lorem ipsum dolor",
      degree: "asdasdasd",
      institution: "consectectur adipicin elit asd.",
      duration: "2019-2023",
      details: "asdasdas rqro  oqro kdkfskd  qeo rqwrka kq.",
    },
    {
      id: "Lorem ipsum dolor",
      degree: "asdasdasd",
      institution: "consectectur adipicin elit asd.",
      duration: "2019-2023",
      details: "asdasdas rqro  oqro kdkfskd  qeo rqwrka kq.",
    },
    {
      id: "Lorem ipsum dolor",
      institution: "consectectur adipicin elit asd.",
      duration: "2019-2023",
      details: "asdasdas rqro  oqro kdkfskd  qeo rqwrka kq.",
    },
  ];
</script>

<template>
      <section class="text-white py-20 overflow-hidden" id="education">
            <!-- Encabezado de la sección -->
            <div class="mb-16">
                  <p class="text-primary text-sm uppercase mb-2 tracking-widest font-semibold">
                        Learning Path
                  </p>
                  <h2 class="text-4xl md:text-5xl font-extrabold text-white">Education</h2>
            </div>

            <!-- Contenedor principal en dos columnas (Imagen izquierda, Lista derecha) -->
            <div class="flex flex-col lg:flex-row items-center lg:items-start gap-16 w-full">
                  
                  <!-- COLUMNA IZQUIERDA: Imagen con efecto sombra -->
                  <div class="w-full lg:w-5/12 flex justify-center lg:justify-start" data-aos="fade-right">
                        <!-- Contenedor con tamaño real asignado -->
                        <div class="relative w-64 h-64 md:w-96 md:h-[450px]">
                              <!-- Borde decorativo trasero -->
                              <div class="absolute inset-0 translate-x-4 translate-y-4 rounded-2xl border-2 border-primary z-0"></div>

                              <!-- Contenedor de la imagen -->
                              <div class="relative z-10 w-full h-full bg-[#111a2e] rounded-2xl overflow-hidden border border-[#1f1641] shadow-lg">
                                    <img :src="educ" alt="Education"
                                          class="w-full h-full object-cover transform transition-transform duration-500 hover:scale-110" />
                              </div>
                        </div>
                  </div>

                  <!-- COLUMNA DERECHA: Lista de contenido Educativo -->
                  <div class="w-full lg:w-7/12 space-y-6" data-aos="fade-left">
                        
                        <!-- El v-for envuelve a toda la tarjeta ahora -->
                        <div v-for="edu in educationData" :key="edu.id" 
                             class="group p-6 rounded-2xl bg-[#1f1641] border border-transparent transition-all duration-300 hover:border-primary/50 shadow-md">
                              
                              <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4">
                                    <div class="flex items-center gap-4">
                                          <!-- Icono del sombrero -->
                                          <div class="p-3 bg-[#050816] rounded-lg border border-primary/20 group-hover:border-primary transition-colors shrink-0">
                                                <GraduationCap class="text-primary" :size="24" />
                                          </div>
                                          
                                          <!-- Textos descriptivos -->
                                          <div>
                                                <h3 class="text-lg font-bold text-white group-hover:text-primary transition-colors">
                                                      
                                                      {{ edu.degree }}
                                                </h3>
                                                <p class="text-gray-400 text-sm">
                                                      {{ edu.institution }}
                                                </p>
                                          </div>
                                    </div>

                                    <!-- Duración / Fechas -->
                                    <span class="text-sm bg-primary/10 text-primary px-3 py-1 bg-[#590202] rounded-full border border-gray-700 w-fit font-medium self-start sm:self-center">
                                          <Calendar :size="15" class="text-primary shrink-0" />
                                          {{ edu.duration }}
                                    </span>
                              </div>

                              <!-- Detalles inferiores opcionales (por si quieres mostrar los detalles de tu array) -->
                              <p class="text-gray-400 text-sm mt-3 pt-3 border-t border-gray-700/30">
                                    {{ edu.details }}
                              </p>

                        </div>

                  </div>
            </div>
      </section>
</template>
