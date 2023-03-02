
<template>
    <div class="profile">
      <div class="card w-96 bg-base-100 shadow-xl">
    <div class="card-body items-center text-center justify-center">
      <h2 class="card-title">
        What I do Today ?
     
      </h2>
      <div class="pekerjaan-rumah justify-center">

        <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="tugas">
           
            <ItemTugas 
            v-bind:tugasSaya="tugasSaya"
            @isDone="isDone(tugasSaya)"/>
            
        </div>
    
      </div>
    </div>
  </div>
      
    </div>
  </template>
  
  <script>
  import ItemTugas from "../components/ItemTugas.vue"

export default{
    name: "todo",
    data : function(){
        return {
            tugas : [
                {
                    id : 1,
                    namaTugas : "Membersihkan muka",
                    isDone : false
                },
                {
                    id : 2,
                    namaTugas : "Membersihkan dosa",
                    isDone : false
                }
            ]
        }
    },
    components : {
        ItemTugas
    },
    methods : {
        isDone(tugasSaya){
            tugasSaya.isDone = !tugasSaya.isDone
        }
    }
}
    </script>
  <style>
  @media (min-width: 1024px) {
    .profile {
      min-height: 100vh;
      display: flex;
      align-items: center;
    }
  }
  </style>
  