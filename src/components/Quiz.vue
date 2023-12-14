<template>
    <v-card class="mx-auto my-8" max-width="344" elevation="16">
        <v-card-item>
            <v-card-title>
                Card title
            </v-card-title>
            <v-card-subtitle>
                Card subtitle secondary text
            </v-card-subtitle>
        </v-card-item>

        <v-card-text>
           {{ quiz_text }}
        </v-card-text>
    </v-card>
</template>
<script>
export default {
    name: 'Quiz',
    props: {
        quiz_text: String
    }
}
</script>