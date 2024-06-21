<template>
  <q-page>
    <q-page-container>
      <div class="q-pa-md q-gutter-md">
        <h4>✦TUGAS 3✦</h4>
        <h1 class="text-center">WEBSITE TODO LIST DENGAN CRUD</h1>
        <div class="flex-center">
          <q-btn 
            flat 
            label="BUKA LINK" 
            href="https://223510251-aziz-tugass3.netlify.app/" 
            target="_blank" 
            class="task-button"
          />
        </div>
      </div>
    </q-page-container>
  </q-page>
</template>

<script>
export default {};
</script>

<style scoped>
.flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.task-button {
  font-size: 1.5rem; 
  padding: 1rem 2rem; 
  border: 2px solid #027be3; 
  border-radius: 8px; 
}

.text-center {
  text-align: center;
}

h4{
  text-align: center;
}
</style>
