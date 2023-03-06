<template>
    <v-container>
        <div id="card">
            <v-avatar color="primary">
                <v-icon dark large>
                    mdi-account
                </v-icon>
            </v-avatar>
            <v-text-field label="login" style="width: 60%;" v-model="loginUser"></v-text-field>
            <v-text-field label="senha" style="width: 60%;" type="password" v-model="senhaUser"></v-text-field>
            <v-btn @click="checaLogin">Entrar</v-btn>
        </div>
    </v-container>
</template>

<script>
export default {
    name: "LoginView",
    data: () => ({
        login: "Admin",
        senha: "admin",
        loginUser: null,
        senhaUser: null,
    }),
    methods: {
        checaLogin() {
            if (this.loginUser == this.login && this.senhaUser == this.senha) {
                this.$router.push('/about')
            } 
            else {
                alert("Login ou senha errado")
            }

        }
    }
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
