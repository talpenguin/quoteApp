<template>
  <div class="row">
    <form style="margin-top: 20px">
      <div
        class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group text-center"
      >
        <label> Quote </label>
        <textarea class="form-control" rows="5" v-model="quote"> </textarea>
      </div>
      <div
        class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group"
      >
        <button class="btn btn-primary col-sm-offset-5 col-xs-offset-5" @click.prevent="createNew">
          Add Quote
        </button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "NewQuote",
  data() {
    return {
      quote: ""
    };
  },
  methods: {
    createNew() {
      this.$emit("addQuote", this.quote);
    }
  }
};
</script>
