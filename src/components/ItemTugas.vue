<template>
     <div class="form-control">
  <label class="cursor-pointer label">
    <input type="checkbox" @click="$emit('isDone')" class="checkbox checkbox-success" />

    <span class="label-text text-justify ml-2">  {{ tugasSaya.namaTugas }}</span>

    <div class="badge badge-accent ml-2" v-if="tugasSaya.isDone">Done</div>
    <div class="badge badge-error ml-2" v-else>Not done</div>
  </label>
</div>
</template>

<script>
export default{
    name:"ItemTugas",
    props:["tugasSaya"]
}
</script>

<style scope>

</style>