<script setup>

    import { defineProps } from 'vue';
    import { RouterLink } from 'vue-router';
    defineProps({
        link: {
            type: String,
            default: '/jobs'
        },
        text: {
            type: String,
            default: 'Job Listings'
        },
    })

</script>

<template>
    <section>
      <div class="container m-auto py-6 px-6">
        <RouterLink
          :to="link"
          class="text-green-500 hover:text-green-600 flex items-center"
        >
          <i class="pi pi-arrow-circle-left mr-2 text-xl"></i> Back To {{ text }}
        </RouterLink>
      </div>
    </section>
</template>