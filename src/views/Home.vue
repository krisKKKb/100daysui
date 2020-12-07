<template>
  <div class="flex-center">
    <div class="home-content">
      <div class="signupcontent">
        <h1>Sign up form</h1>
        <div class="usern">
          Kasutajanimi
          <input name="username" placeholder="Sisestage kasutajanimi" />
        </div>
        <div class="pw">
          Parool
          <input
            name="password"
            placeholder="Sisestage parool"
            type="password"
          />
        </div>
        <div class="signup">
          <button>Sign up</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
};
</script>

<style lang="scss">
.flex-center {
  display: flex;
  justify-content: center;
}
.home {
  &-content {
    max-width: 50vh;
    min-width: 400px;
  }
}
.signupcontent {
  background: lightgray;
}
.pw {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-top: 1rem;
}
.usern {
  display: flex;
  flex-direction: column;
  padding-top: 1rem;
  justify-content: center;
}
.signup {
  padding: 1rem;
}
</style>
