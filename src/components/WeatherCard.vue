<template>
  <div>
    <div class="card mb-3">
      <div class="card-body">
        <h5 class="card-title">{{ username }}</h5>
        <h6 class="card-subtitle mb-2 text-muted">{{ companyName }}</h6>
        <h6 class="card-subtitle mb-2 text-muted">{{ email }}</h6>
        <a href="#" class="card-link">{{ websiteLink }}</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    username: {
      type: String,
      required: true
    },
    companyName: {
      type: String,
      required: true
    },
    email: {
      type: String,
      required: true
    },
    websiteLink: {
      type: String,
      required: true
    }
  }

};
</script>

