<template>
    <v-card class="mx-auto my-2 h-25" width="200"   elevation="14">
        <v-card-item>
            <v-card-title>
                {{ title }}
            </v-card-title>
            <!-- <v-card-subtitle>
                Card subtitle secondary text
            </v-card-subtitle> -->
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
        title: String,
        quiz_text: String
    }
}
</script>