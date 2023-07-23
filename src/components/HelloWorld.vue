<template>
  <div class="border flex justify-center flex-col">
    <button @click="showForm = true" v-if="!showForm">Show Form</button>
    <button @click="showForm = false" v-else>Show Data</button>


    <div class="flex justify-center items-center flex-col" :class="showForm ? 'h-[28rem]' : 'h-[35rem]'">
      <div v-if="showForm" class="w-full">
        <FormComponent />
      </div>

      <div v-else>
        <ShowData />
      </div>
    </div>
  </div>
</template>

<script>
import FormComponent from "@/components/FormComponent.vue"
import ShowData from "@/components/ShowData.vue";

export default {
  name: 'App',
  components: {
    FormComponent,
    ShowData
  },
  data() {
    return {
      showForm: true,

    };
  }
};
</script>
