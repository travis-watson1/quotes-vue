<template>
    <div class="row text-center">
        <form>
        <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 text-center">
            <label class="default-margin">Enter Quote:</label>
            <textarea rows="3" class="form-control default-margin" v-model="quote"></textarea>
        </div>
                <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 text-center">
            <button class="btn btn-primary default-margin" @click.prevent="createNew">New Quote</button>
        </div>
        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                quote: ''
            };
        },
        methods: {
            createNew() {
                this.$emit('quoteAdded', this.quote);
                this.quote = '';
            }
        }
    }
</script>

<style>

</style>

