<script setup>
import { ref } from 'vue'

const novaTarefa = ref('')
const tarefas = ref([])

function adicionar() {
  if (novaTarefa.value.trim() !== '') {
    tarefas.value.push({ texto: novaTarefa.value, concluida: false })
    novaTarefa.value = ''
  }
}

function remover(index) {
  tarefas.value.splice(index, 1)
}
</script>

<template>
  <div style="font-family: Arial, sans-serif; max-width: 400px; margin: 40px auto; padding: 20px; border: 1px solid #ccc; border-radius: 8px;">
    <h2 style="color: #42b883;">Vue Tasker</h2>
    
    <div style="display: flex; gap: 10px; margin-bottom: 20px;">
      <input v-model="novaTarefa" placeholder="Digite uma tarefa..." @keyup.enter="adicionar" style="flex: 1; padding: 8px;" />
      <button @click="adicionar" style="background-color: #42b883; color: white; border: none; padding: 8px 12px; cursor: pointer; border-radius: 4px;">Add</button>
    </div>

    <ul style="list-style: none; padding: 0;">
      <li v-for="(t, index) in tarefas" :key="index" style="display: flex; justify-content: space-between; margin-bottom: 10px; align-items: center;">
        <div>
          <input type="checkbox" v-model="t.concluida" style="margin-right: 10px;">
          <span :style="{ textDecoration: t.concluida ? 'line-through' : 'none' }">{{ t.texto }}</span>
        </div>
        <button @click="remover(index)" style="background-color: #ff4d4f; color: white; border: none; padding: 4px 8px; border-radius: 4px; cursor: pointer;">X</button>
      </li>
    </ul>
  </div>
</template>