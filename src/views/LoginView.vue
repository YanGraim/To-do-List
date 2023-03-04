<template>
    <v-container>
        <div id="card">
            <v-avatar color="primary">
                <v-icon dark large>
                    mdi-account
                </v-icon>
            </v-avatar>
            <v-text-field name="name" label="login" id="id" style="width: 60%;"></v-text-field>
            <v-text-field name="name" label="senha" id="id" style="width: 60%;" type="password"></v-text-field>
            <v-btn>Entrar</v-btn>
        </div>
    </v-container>
</template>

<script>
export default {
    name: "LoginView",
};
</script>

<style>
#card {
    background-color: #fffafa05;
    border: 1px solid gray;
    padding: 1rem;
    max-width: 500px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}
</style>
