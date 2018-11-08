<template>
    <div>
        <b-navbar toggleable type="dark" variant="dark">
            <b-navbar-toggle target="nav_text_collapse"></b-navbar-toggle>
            <b-navbar-brand>Dashboard</b-navbar-brand>
            <b-collapse is-nav id="nav_text_collapse">
                <b-navbar-nav>
                    <b-nav-item href="#">Fiche salarié</b-nav-item>
                    <b-nav-item href="#">Planning</b-nav-item>
                    <b-nav-item href="#">Absences</b-nav-item>
                </b-navbar-nav>
            </b-collapse>
        </b-navbar>
    </div>
</template>

<script>
export default {
  name: 'dashboard'
}
</script>

<style scoped>

</style>
