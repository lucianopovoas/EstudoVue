<template>
  <div>
    <h1>{{ teste }}</h1>
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
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycleHook from './components/LifeCycleHook/LifeCycleHook.vue'
import CandidatoPessoa from './components/CandidatoFormulario/CandidatoPessoa.vue';
import CadastroPessoa from './components/Diretivas/CadastroPessoa.vue';
import AtributoVBind from './components/AtributosDinamicos/AtributoVBind.vue';
import AtributoResumido from './components/AtributosDinamicos/AtributoResumido.vue';
import MetodosVue from './components/Metodos/MetodosVue.vue';

  export default{
    name: 'App',
    components:{
      PrimeiroComponente,
      LifeCycleHook,
      CandidatoPessoa,
      CadastroPessoa,
      AtributoVBind,
      AtributoResumido,
      MetodosVue
    },
    data(){
      return{
        teste: "teste"
      }
    }
  }
</script>
