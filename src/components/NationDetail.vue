<template>
    <div class="nation-detail" v-if="showDetail">
        <div>
            <div>
                <h3>{{ nation.name }}<span @click="$emit('closeModal')">X</span></h3>
            </div>
            <img :src="nation.symbol">
            <p>{{ nation.description }}</p>
        </div>
    </div>
</template>
<script>
export default {
    props : {
        showDetail : Boolean,
        nation : Object
    }
}
</script>