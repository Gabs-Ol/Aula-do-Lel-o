<template>
    <section>
        <div>
            <p>Meu Conteúdo Raso e Fútil</p>
            <div>
                <input v-model="nome" placeholder="Digite seu Nome">
                <p>Seu Nome é: {{ nome }}</p>
                <button @click="submeterFormulário()">Verificar Nome</button>

                <p v-if="url">
                    {{  url  }}
                </p>
            </div>
        </div>
    </section>
</template>

<script>

export default {
    name:'ContentPage',
    data() {
        return{
            nome: 'Filho do Bill Amostradinho Só Fé da Silva'
        }
    },
    methods: {
        submeterFormulário() {
            let response =
            fetch.get('https://api.github.com/users/${this.nome}').then(() => {
                this.url = data.url;
                console.log(data.url);
            });

            console.log(response);
        }
    }
}
</script>