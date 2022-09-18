<template>
  <div
    class="container-fluid mt-5 d-flex flex-wrap justify-content-center align-items-center"
  >
    <form style="width: 500px" @submit.prevent="onSubmit">
      <fieldset>
        <legend v-if="isUpdate">Köse Yazısı Düzenle</legend>
        <legend v-else>Köse Yazısı Oluştur</legend>
        <div class="form-group">
          <label>Yazar Adı</label>
          <input
            v-model="post.author"
            type="text"
            class="form-control"
            placeholder="Yazarın adını giriniz.."
          />
        </div>
        <div class="form-group">
          <label>Baslık</label>
          <input
            v-model="post.title"
            type="text"
            class="form-control"
            placeholder="Yazının baslıgını giriniz.."
          />
        </div>
        <div class="form-group">
          <label>Alt Baslık</label>
          <input
            v-model="post.subTitle"
            type="text"
            class="form-control"
            placeholder="Yazının alt baslıgını giriniz.."
          />
        </div>
        <div class="form-group">
          <label for="exampleTextarea">Köse Yazısı</label>
          <textarea
            v-model="post.text"
            class="form-control"
            rows="5"
          ></textarea>
        </div>
        <button @click="$router.push('/admin')" class="btn btn-danger">İptal</button>
        <button type="submit" class="btn btn-primary">Kaydet</button>
      </fieldset>
    </form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      post: {
        title: null,
        author: null,
        subTitle: null,
        text: null,
      },
    };
  },
  props: {
    isUpdate: {
      type: Boolean,
      required: false,
      default:false
    },
  },
  methods: {
    onSubmit() {
      this.$emit("submit", this.post);
    },
  },
};
</script>
