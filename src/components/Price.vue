<template>
    <v-form>
        <v-container class="ml-3">
            <!-- Precio -->
            <v-row class="my-3 ml-2">
                Precio por
            </v-row>
            <v-row class="my-3 ml-4">
                <!-- Unit -->
                <v-col
                    cols="12"
                    md="3"
                >
                    <v-select
                        label="Unidad"
                        :items="units"
                        v-model="selectedUnit"
                        item-text="text"
                        outlined
                    ></v-select>
                </v-col>

                <!-- Price -->
                <v-col
                    cols="12"
                    md="3"
                >
                    <v-text-field
                        label="Precio por Kg"
                        type="tel"
                        outlined
                        cols="3"
                        v-model="pricePerUnit"
                    >
                    </v-text-field>
                </v-col>
            </v-row>

            <!-- Consulta -->
            <v-row class="my-3 ml-2">
                Consulta
            </v-row>
            <v-row class="my-3 ml-4">
                <!-- Price -->
                <v-col
                    cols="12"
                    md="3"
                >
                    <v-text-field
                        label="Cantidad"
                        type="tel"
                        outlined
                        cols="3"
                        v-model="quantity"
                    >
                    </v-text-field>
                </v-col>

                <!-- Unit -->
                <v-col
                    cols="12"
                    md="3"
                >
                    <v-select
                        label="Unidad"
                        :items="quantityUnits"
                        v-model="selectedQuantityUnit"
                        item-text="text"
                        outlined
                    ></v-select>
                </v-col>
            </v-row>
        </v-container>
    </v-form>
</template>

<script>
export default {
    data() {
        return {
            /// Precio
            selectedUnit: {},
            units: [
                { text: 'Kilogramo (Kg)' },
                { text: 'Gramo (g)' }
            ],
            pricePerUnit: null,
            // Consulta
            quantity: null,
            selectedQuantityUnit: null,
            quantityUnits: [
                { text: 'Kilogramo (Kg)' },
                { text: 'Gramo (g)' }
            ],
        }
    },
}
</script>

<style>

</style>