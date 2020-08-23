<template>
  <div>
    <div id="slogan" class="text-center">
      <h1>NameGator</h1>
    <br>
    <h6 class="text-secondary">Gerador de nomes</h6>
    </div>
    <div id="main">
      <div class="container">
        <div class="row">
        <div class="col-md">
          <h5>Prefixos <span class="badge badge-info">{{ prefixes.length }}</span></h5>
          <div class="card">
            <div class="card-body">
              <ul class="list-group">
              <li class="list-group-item" v-for="prefix in prefixes" v-bind:key="prefix">
                {{ prefix }}
              </li>
            </ul>
            </div>
            <input class="form-control" type="text" placeholder="Digite seu Prefixo">
          </div>
        </div>
        <div class="col-md">
          <h5>Sufixos <span class="badge badge-info">{{ sufixes.length }}</span></h5>
          <div class="card">

            <div class="card-body">
              <ul class="list-group">
              <li class="list-group-item" v-for="sufix in sufixes" v-bind:key="sufix">
                {{ sufix }}
              </li>
            </ul>
            </div>
            <input class="form-control" type="text" placeholder="Digite seu Sufixo">
          </div>
        </div>
      </div>
      <br>
      <h5>Dominios <span class="badge badge-info">{{ domains.length }}</span></h5>
    <div class="card">
            <div class="card-body">
              <ul class="list-group">
                <li class="list-group-item" v-for="domain in domains" v-bind:key="domain">
                  {{ domain }}
                </li>
              </ul>
            </div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css';
import 'font-awesome/css/font-awesome.css';

export default {
  name: 'app',
  data() {
    return {
      prefixes: ['Air', 'Hub', 'Be'],
      sufixes: ['Cap', 'Food', 'Mac'],
      domains: ['AirCap', 'AirFood', 'AirMac', 'HubCap'],
    };
  },
};

</script>

<style>
#slogan {
  margin-top: 30px;
}
#main{
  background-color: blanchedalmond;
  padding-top: 30px;
  padding-bottom: 30px;
}
</style>
