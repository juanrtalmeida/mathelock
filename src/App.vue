<template>
  <div class="pagecontainer">
    <Header />
    <div class='operationBox'>
      <input type="text" maxlength="1" v-model="number"  @input="verifyNumber"/>
        <select name="operacao" id="">
          <option value={+}>+</option>
          <option value={-}>-</option>
          <option value={/}>/</option>
          <option value={*}>x</option>
        </select>
      <input type="text" maxlength="1" v-model="number"  @input="verifyNumber"/>
        <select name="operacao" id="">
          <option value={+}>+</option>
          <option value={-}>-</option>
          <option value={/}>/</option>
          <option value={*}>x</option>
        </select>
      <input type="text" maxlength="1" v-model="number"  @input="verifyNumber"/>
        <select name="operacao" id="">
          <option value={+}>+</option>
          <option value={-}>-</option>
          <option value={/}>/</option>
          <option value={*}>x</option>
        </select>
      <input type="text" maxlength="1" v-model="number"  @input="verifyNumber"/>
      <p> = {{dayNumber}}</p>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
export default {
  name: "App",
  components: {
    Header,
  },
  data() {
    return {
      number: "",
      dayNumber: 322,
    };
  },

  mounted() {
    setInterval(() => {
      this.count++;
    }, 1000);
  },
  methods: {
    verifyNumber: function (event) {
      const result = Number(event.target.value);

      if (isNaN(result)) {
        this.number = "";
      }
    },
  },
};
</script>

<style scoped>


#app {
  font-family: sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  list-style: none;
}

.pagecontainer {
  display: flex;
  height: 100vh;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.operationBox {
  margin-top: 50px;
  display: flex;
  width: 100%;
  justify-content: space-around;
}
.operationBox input {
  background-color: transparent;
  border: 4px solid rgba(34, 33, 33, 0.753);
  font-size: 5rem;
  width: 5rem;
  text-align: center;
  border-radius: 10px;
  color: rgb(130, 212, 185);
}
.operationBox input:focus {
  outline: #005ebd;
}
.operationBox form {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
p {
  font-family: "Poppins";
  font-weight: 300;
  color: rgb(130, 212, 185);
  font-size: 5rem;
  
}

.operationBox select {
  background-color: transparent;
  border: none;
  border-radius: 10px;
  font-size: 5rem;
  color: rgb(130, 212, 185);
  text-align: center;
  width: 5rem;

  -webkit-appearance: none;

  text-indent: 1px;
  text-overflow: "";
}
.operationBox select option {
  background-color: #2c3e50;
}


@media(min-width: 466px)and (max-width:820px) {
  .operationBox input{
      font-size: 3rem;
      width: 3rem;
  }

  p {
  font-size: 3rem;
}

  .operationBox select{
     font-size: 3rem;
  width: 3rem;
  }
 

}


@media(max-width:466px) {
  .operationBox input{
      font-size: 2rem;
      width: 2rem;
  }

  p {
  font-size: 2rem;
}

  .operationBox select{
     font-size: 2rem;
  width: 2rem;
  }
 

}
</style>
