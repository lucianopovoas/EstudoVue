<template>
  <div>
    <h1 class="primeiroH1">{{ teste }}</h1>
    <PrimeiroComponente />
    <LifeCycleHook />
    <CandidatoPessoa />
    <HeaderScoped />
  </div>
<hr>

  <div>
    <DiretivaVshow />
    <DiretivaVBind />
    <DiretivaVBindResumido />
    <DiretivaVfor />
    <DiretivaVmodel />
    <DiretivaVon />
  </div>
<hr>

  <div>
    <MetodosVue /> 
    <EventosVue />
    <MultiplosEventos />
  </div>
<hr>

  <div>
    <ComputedPropriedade />
    <WatchObservadores />
  </div>
<hr>

  <div>
    <SlotComponent/>
    <PropsDado variante="success"/>
    <EmitDado v-if="showEmit" @close="onClose()" />
  </div>

  <div>
    <ApiComposition />
  </div>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycleHook from './components/LifeCycleHook/LifeCycleHook.vue'
import CandidatoPessoa from './components/CandidatoFormulario/CandidatoPessoa.vue';
import HeaderScoped from './components/CssScoped/HeaderScoped.vue';

import DiretivaVshow from './components/vshow/CadastroPessoa.vue';
import DiretivaVBind from './components/vbind/AtributoVBind.vue';
import DiretivaVBindResumido from './components/vbind/AtributoResumido.vue';
import DiretivaVfor from './components/vfor/ArrayPercorrendo.vue';
import DiretivaVmodel from './components/vmodel/DiretivaVmodel.vue';
import DiretivaVon from './components/von/DiretivaVon.vue';

import MetodosVue from './components/Metodos/MetodosVue.vue';
import EventosVue from './components/EventosSubmitClick/Eventos.vue';
import MultiplosEventos from './components/MultiplosEventos/MultiplosEventos.vue';

import ComputedPropriedade from './components/Computed/ComputedPropriedade.vue';
import WatchObservadores from './components/Watch/WatchObservadores.vue';

import SlotComponent from './components/Slot/SlotComponent.vue';
import PropsDado from './components/Props/PropsDado.vue';
import EmitDado from './components/Emit/EmitDado.vue';

import ApiComposition from './components/ApiComposition/ApiComposition.vue';

  export default{
    name: 'App',
    components:{
      PrimeiroComponente,
      LifeCycleHook,
      CandidatoPessoa,
      HeaderScoped,
      DiretivaVshow,
      DiretivaVBind,
      DiretivaVBindResumido,
      DiretivaVfor,
      DiretivaVmodel,
      DiretivaVon,
      MetodosVue,
      EventosVue,
      MultiplosEventos,
      ComputedPropriedade,
      WatchObservadores,
      SlotComponent,
      PropsDado,
      EmitDado,
      ApiComposition,
    },
    data(){
      return{
        teste: "teste",
        showEmit: true
      }
    },
    methods:{
      onClose(){
        this.showEmit = false
        console.log("on close")
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