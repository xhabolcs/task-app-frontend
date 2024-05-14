<script setup lang="ts">
const items = [
  {
    description: 'Go to shop',
    userId: '1',
    estimatedTime: '2h',
    usedTime: '1h',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Clean the kitchen',
    userId: '2',
    estimatedTime: '1h',
    usedTime: '',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Maintain the bike',
    userId: '3',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Ride the bike',
    userId: '4',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Go hike',
    userId: '5',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Drink water',
    userId: '6',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Play football',
    userId: '7',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Do the job',
    userId: '8',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Obey the rules',
    userId: '9',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Have fun',
    userId: '10',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Star gazing',
    userId: '11',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Go to Békéscsaba',
    userId: '12',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Kiss your girlfriend',
    userId: '13',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  },
  {
    description: 'Be happy',
    userId: '14',
    estimatedTime: '1h ',
    usedTime: '30m',
    createdAt: new Date(),
    completedAt: new Date()
  }
]

let selected: any[] = []
</script>

<template>
  <v-app>
    <v-container>
      <v-data-table
        v-model="selected"
        :items="items"
        :header-props="{ 'sort-icon': 'mdi-triangle-down' }"
      ></v-data-table>
    </v-container>
  </v-app>
</template>
