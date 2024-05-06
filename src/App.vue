<template>
  <div>
    <h1 class="primeiroH1">{{ teste }}</h1>
    <PrimeiroComponente />
    <LifeCycleHook />
    <CandidatoPessoa />
  </div>
  <div>
    <CadastroPessoa />
  </div>
  <div>
    <AtributoVBind />
    <AtributoResumido />
  </div>
  <div>
    <MetodosVue />
  </div>
  <div>
    <HeaderScoped />
  </div>
  <div>
    <ArrayPercorrendo />
  </div>
  <div>
    <EventosVue />
    <MultiplosEventos />
  </div>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycleHook from './components/LifeCycleHook/LifeCycleHook.vue'
import CandidatoPessoa from './components/CandidatoFormulario/CandidatoPessoa.vue';
import CadastroPessoa from './components/Diretivas/CadastroPessoa.vue';
import AtributoVBind from './components/AtributosDinamicos/AtributoVBind.vue';
import AtributoResumido from './components/AtributosDinamicos/AtributoResumido.vue';
import MetodosVue from './components/Metodos/MetodosVue.vue';
import HeaderScoped from './components/CssScoped/HeaderScoped.vue';
import ArrayPercorrendo from './components/RenderizacaoDeLista/ArrayPercorrendo.vue';
import EventosVue from './components/EventosSubmitClick/Eventos.vue';
import MultiplosEventos from './components/MultiplosEventos/MultiplosEventos.vue';

  export default{
    name: 'App',
    components:{
      PrimeiroComponente,
      LifeCycleHook,
      CandidatoPessoa,
      CadastroPessoa,
      AtributoVBind,
      AtributoResumido,
      MetodosVue,
      HeaderScoped,
      ArrayPercorrendo,
      EventosVue,
      MultiplosEventos
    },
    data(){
      return{
        teste: "teste"
      }
    }
  }
</script>

<style>
  body{
   background-color: #221f1f; 
   color: white;
  }
  a{
    color: red
  }
</style>