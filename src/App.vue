<template>
  <div id="app">
    <Navbar/>
    <section>
      <img src="./assets/mainImage.png">
    </section>
    <section class="section is-medium is-primary has-text-centered">
      <div class="container">
        <div class="columns is-centered">
          <div class="column is-three-fifths">
            <h1 class="title is-spaced is-size-3-desktop is-size-4-mobile"> {{ titulo }}</h1>
            <h2 class="subtitle is-size-5-desktop">
              {{ mensagem }}
            </h2>
          </div>
        </div>
      </div>
    </section>
    <div class="container is-fluid notification">
        <router-view/>
    </div>
    <footer class="footer">
      <div class="content has-text-centered">
        <p><strong>Desenvolvido</strong> por <a href="https://jgthms.com">RH Team</a>.</p>
      </div>
    </footer>
  </div>
</template>

<script>
import Navbar from './components/Navbar'
export default {
  name: 'App',
  components: { Navbar },
  data () {
    return {
      titulo: 'It Happens',
      mensagem: 'Somos uma software house que gerencia múltiplos núcleos, como: RH, Compras, Vendas, Força de Vendas, Estoque, WMS, Contabilidade, Financeiro, E-commerce, Estatística, Infraestrutura, Frente de loja (PDV), CRM, Chatbot e Catch Up. Com profissionais capacitados na execução de projetos customizados, especializada em serviços e soluções tecnológicas para o mercado de varejo, atacado, eletro e indústria, buscando sempre ultrapassar novos desafios em constante aprendizado.'
    }
  },
  methods: {
  }
}
</script>
