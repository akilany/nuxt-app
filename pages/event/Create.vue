<template>
  <div class="create">
          <h1>Create Event</h1>
      <div class="container">
          <form class="form">
              <input type="text" class="field" placeholder="Title">
              <input type="text" class="field" placeholder="Field">
              <button class="btn">Create</button>
          </form>
      </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Create Event',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'This is create page.'
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content: 'create page, create, create main'
        }
      ]
    }
  }
}
</script>

<style>
.create {
  padding: 4rem 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

h1 {
  margin: 1rem 0 2rem;
}
.form {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 100%;
}

.form .field {
  width: 450px;
  padding: 1rem;
  border: none;
  border: 1px solid #eee;
  background: #f8f8f8;
  margin-bottom: 1rem;
  transition: all 0.3s ease-out;
  border-radius: 5px;
}

.field:hover {
  border: 1px solid rgb(41, 189, 209);
}

.btn {
  margin-top: 1rem;
  padding: 0.7rem 1.5rem;
  text-transform: uppercase;
  background: rgb(41, 189, 209);
  border: none;
  border-radius: 5px;
  color: #fff;
  cursor: pointer;
}
</style>