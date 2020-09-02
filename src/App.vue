<template>
  <div id="app">
    <div class="form-group">
      <label>CPF sem máscara</label>
      <div>
        <input type="text" v-model="cpf" />
      </div>
    </div>
    <div class="form-group">
      <label>CPF</label>
      <div>
        <the-mask
          :masked="true"
          v-model="cpfComMascara"
          :mask="'###.###.###-##'"
        />
      </div>
    </div>
    <div class="form-group">
      <label>Telefone (8 ou 9 dígitos)</label>
      <div>
        <the-mask
          v-model="telefoneMask"
          :mask="['(##) ####-####', '(##) #####-####']"
        />
      </div>
    </div>
    <div class="form-group">
      <label>Informe a sua idade</label>
      <div>
        <el-input-number
          v-model="idade"
          :min="1"
          :max="150"
          placeholder="idade"
          size="small"
        ></el-input-number>
      </div>
    </div>
    <div class="form-group">
      <label>Data de nascimento</label>
      <div>
        <el-date-picker
          v-model="dataNascimento"
          type="date"
          placeholder="Data nascimento"
          format="dd/MM/yyyy"
          value-format="dd/MM/yyyy"
          size="small"
        >
        </el-date-picker>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      cpf: "",
      cpfComMascara: "",
      telefoneMask: "5199995555",
      idade: 1,
      dataNascimento: null,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
