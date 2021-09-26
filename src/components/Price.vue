<template>
    <div>
        <v-col
            class="mt-5"
            cols="12"
            sm="6"
            md="3"
        >
            <h3 class="mb-4">
                Consulta
            </h3>
            <!-- Price -->
            <v-text-field
                label="Precio"
                type="tel"
                outlined
            >
            </v-text-field>
            <!-- Unit -->
            <v-select
                label="Unidad"
                :items="units"
                v-model="selectedUnit"
                item-text="name"
                outlined
            ></v-select>

            <v-divider
                class="mb-6"
            ></v-divider>

            <h3 class="mb-4">
                Respuesta
            </h3>

            <!-- Target Unit -->
            <v-select
                label="Unidad Objetivo"
                :items="units"
                v-model="selectedTargetUnit"
                item-text="name"
                outlined
            ></v-select>
            <!-- Price -->
            <v-text-field
                label="Precio Objetivo"
                type="tel"
                outlined
                readonly
            >
            </v-text-field>
        </v-col>
    </div>
</template>

<script>
export default {
    data() {
        return {
            price: null,
            selectedUnit: 'Kilogramo (g)',
            selectedTargetUnit: 'Kilogramo (g)',
            units: [
                'Kilogramo (Kg)',
                'Gramo (g)'
            ],
        }
    },
}
</script>

<style>

</style>