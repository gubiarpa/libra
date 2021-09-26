<template>
    <div>
        <!-- Textbox Price -->
        <v-col
            cols="12"
            sm="6"
            md="3"
        >
            <v-text-field
                label="Precio"
                type="tel"
                outlined
            >
            </v-text-field>
        </v-col>
        
        <!-- Unit -->
        <v-col
            cols="12"
            sm="6"
            md="3"
        >
            <v-select
                label="Unidad"
                :items="units"
                v-model="selectedUnit"
                item-text="name"
                outlined
                ></v-select>
        </v-col>
    </div>
</template>

<script>
export default {
    data() {
        return {
            price: null,
            selectedUnit: 'Kilogramo (g)',
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