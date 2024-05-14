<script setup lang="ts">
import { ref } from 'vue'

interface ToDos {
  id: string
  userId: string
  description: string
  estimatedTime: string
  usedTime: string
  createdAt: Date
  completedAt: Date
}

const headers = [
  { title: 'Id', key: 'id' },
  { title: 'User Id', key: 'userId' },
  { title: 'Description', key: 'description' },
  { title: 'Estimated Time', key: 'estimatedTime' },
  { title: 'Used Time', key: 'usedTime' },
  { title: 'Created At', key: 'createdAt' },
  { title: 'Completed At', key: 'completedAt' }
]

const selected = ref<ToDos[]>([])

const items: ToDos[] = [
  {
    id: '1',
    userId: '1',
    description: 'Go to shop',
    estimatedTime: '2h',
    usedTime: '1h',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '2',
    userId: '2',
    description: 'Clean the kitchen',
    estimatedTime: '1h',
    usedTime: '',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '3',
    userId: '3',
    description: 'Maintain the bike',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '4',
    userId: '1',
    description: 'Ride the bike',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '5',
    userId: '2',
    description: 'Go hike',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '6',
    userId: '3',
    description: 'Drink water',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '7',
    userId: '1',
    description: 'Play football',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '8',
    userId: '2',
    description: 'Do the job',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '9',
    userId: '3',
    description: 'Obey the rules',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '10',
    userId: '1',
    description: 'Have fun',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '11',
    userId: '2',
    description: 'Star gazing',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '12',
    userId: '3',
    description: 'Go to Békéscsaba',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '13',
    userId: '1',
    description: 'Kiss your girlfriend',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    id: '14',
    userId: '2',
    description: 'Be happy',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  }
]

const onSelectionUpdate = (newSelection: ToDos[]) => {
  selected.value = newSelection
}
</script>

<template>
  <v-data-table
    id="table"
    show-select
    select-strategy="page"
    :items="items"
    :headers="headers"
    item-key="id"
    class="elevation-1"
    :model-value="selected"
    @update:model-value="onSelectionUpdate"
  >
  </v-data-table>
</template>
