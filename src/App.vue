<template>
  <button @click="addFirstName"> Add First Name</button>
</template>

<script setup>
  import {ref,onMounted} from "vue"
  // import $ from "jquery"
  import Editor from "datatables.net-editor";


  onMounted(()=>{
    // console.log(new $.fn.dataTable.Editor)
  })


  const editorFirstName = new Editor({
      fields: [
          {
              label: 'Fist Name:',
              name: 'firstname',
              type : 'text',
          },
      ]
  })

  const addFirstName = ()=> {
    editorFirstName.create({
        title : "Add First Name"
    }) //
  }
</script>

