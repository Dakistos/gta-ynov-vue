<template>
    <div class="hello">
        <h1>{{msg}}</h1>
            <div class="connect">
                <b-form-input placeholder="Identifiant" class="input-connect" v-model="input.username" name="username"></b-form-input>
                <b-form-input placeholder="Mot de passe" class="input-connect" type="password" v-model="input.password" name="password"></b-form-input>
                <b-button variant="primary" v-on:click="connection()">Se connecter</b-button>
                <b-button variant="link" v-on:click="goToSignup()">S'inscrire</b-button>
            </div>
    </div>
</template>

<script>
import router from '../router'
import donnee from '../data.json'

export default {
  name: 'HelloWorld',

  data () {
    return {
      msg: 'Gestion des Temps et des Activités',
      userData: donnee,
      input: {
        username: '',
        password: ''
      }
    }
  },

  methods: {
    connection () {
      if (this.input.username != '' && this.input.password != '') {
        if (this.input.username == this.userData.username && this.input.password == this.userData.password) {
          router.replace({name: 'dashboard'})
        } else {
          console.log('Identifiant ou mot de passe incorrect')
        }
      } else {
        console.log('Entrer un identifiant et un mot de passe')
      }
    },

    goToSignup: function () {
      router.push({name: 'signup'})
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .connect{
        margin-top: 20px;
    }
    .input-connect {
        width: 50%;
        margin: 10px auto;
    }
</style>
