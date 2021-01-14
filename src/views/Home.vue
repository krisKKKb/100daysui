<template>
  <body>
    <div class="flex-center">
      <div class="home-content">
        <div class="signupcontent">
          <h1>Sign up form</h1>
          <div class="email">
            E-mail
            <input name="email" placeholder="Sisestage e-mail" />
          </div>
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
            <button class="signupbtn">Sign up</button>
          </div>
        </div>
      </div>
    </div>
  </body>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
};
</script>

<style lang="scss">
body {
  background: linear-gradient(0.25turn, #00f208, #00fad0, #00aeff);
}

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
.email {
  display: flex;
  margin-left: 7.5rem;
  flex-direction: column;
  justify-content: center;
  padding-top: 1rem;
  width: 10rem;
}
.pw {
  display: flex;
  margin-left: 7.5rem;
  flex-direction: column;
  justify-content: center;
  padding-top: 1rem;
  width: 10rem;
}
.usern {
  display: flex;
  margin-left: 7.5rem;
  flex-direction: column;
  padding-top: 1rem;
  justify-content: center;
  width: 10rem;
}
.signup {
  padding: 1.5rem;
}
.signupbtn {
  background: linear-gradient(#08c94c, #21ff6f, #bfffd6);
  width: 250px;
  height: 50px;
  font-size: 1rem;
  border-radius: 100px;
  text-decoration: none;
}
</style>
