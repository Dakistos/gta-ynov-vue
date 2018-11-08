<template>
    <div class="signup-size">
        <h1>Création d'un compte</h1>
        <div class="connect">
            <b-form-input placeholder="Identifiant" class="input-connect"></b-form-input>
            <b-form-input placeholder="Mot de passe" class="input-connect" type="password"></b-form-input>
            <b-form-input placeholder="Confirmer le mot de passe" class="input-connect" type="password"></b-form-input>
            <b-button variant="primary">S'inscire</b-button>
        </div>
    </div>
</template>

<script>
export default {
  name: 'signup',
  date () {
    return {

    }
  }
}
</script>

<style scoped>
    .connect{
        margin-top: 20px;
    }
    .input-connect {
        width: 50%;
        margin: 10px auto;
    }
</style>
