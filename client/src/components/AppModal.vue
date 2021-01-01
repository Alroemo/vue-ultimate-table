<template>
    <div>
        <h1>Ultimate Table</h1>
        <span>The sexy snazy Table</span>

        <b-tabs content-class="mt-3">
            <b-tab title="First" active>
                <UltimateTable/>
            </b-tab>
            <b-tab title="Second"><p>I'm the second tab</p></b-tab>
            <b-tab title="Disabled" disabled><p>I'm a disabled tab!</p></b-tab>
        </b-tabs>
    </div>
</template>

<script>
import UltimateTable from './Table.vue'

export default {
    components: {
        UltimateTable
    }
}
</script>

