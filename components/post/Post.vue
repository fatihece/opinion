<template>
  <div class="card mr-3 mb-3 card-success" style="width: 18rem">
    <div class="card-body">
      <h5 class="card-title">Card title</h5>
      <h6 class="card-subtitle mb-2 text-muted">Card subtitle</h6>
      <p class="card-text">
        Some quick example text to build on the card title and make up the bulk
        of the card's content.
      </p>
   
      <div class="admin-button-container" v-if="isAdmin">
        <a
          href="#"
          @click.prevent="$router.push('/admin/1')"
          class="btn btn-outline-warning btn-sm"
          >Düzenle</a
        >
        <a href="#" class="btn btn-outline-danger btn-sm">Sil</a>
      </div>
      <a
      v-else
        href="#"
        @click.prevent="$router.push('/posts/1')"
        class="btn btn-outline-info btn-sm" 
        >Görüntüle</a>
    </div>
  </div>
</template>
<script>
export default{
    props:{
        isAdmin:{
            type:Boolean,
            required:true,
        }
    }
}


</script>
