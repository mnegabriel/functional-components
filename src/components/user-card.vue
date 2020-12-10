<template functional> 
<div class="card" @click="listeners.click">
        <div class="additional">
          <button @click.stop="listeners.contact">alert two</button>
          <figure class="avatar">
            <img :src="props.user.avatar" :alt="props.user.name" />
          </figure>
        </div>
        <div class="more-info">
          <h1>{{ props.user.name }}</h1>
          <h3>{{ props.user.role }}</h3>
          <p>
            <slot name='body' />
          </p>
          <!-- <p>{{Object.keys(listeners)}}</p> -->
        </div>
      </div>
</template>

<script>
  export default {
    name: 'Card',

    // props: {
    //   user: Object,
    // },
  };
</script>
