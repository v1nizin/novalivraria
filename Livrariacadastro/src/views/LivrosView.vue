<script>
export default {
  data() {
    return {
      livros: [
    
      ],
      novo_livro: "",
    };
  },
  methods: {
    salvar() {
      
      this.livros.push({
        
        nome: this.novo_livro,
          });
        },
      },
    };
</script>

<template>
  <div class="container">
    <div class="title">
    
    
    <div>
        <h2>Categorias</h2>
      <select name="select">
        <option value=""></option>
        <option value="">Terror</option>
        <option value="">Suspense</option>
        <option value="">Aventura</option>
        <option value="">Ação</option>
        <option value="">Comédia</option>
        <option value="">Fantasia</option>
        <option value="">Ficção Cientifica</option>
        <option value="">Drama</option>
        <option value="">Infantil</option>
        <option value="">Romance</option>
        <option value="">Mistério</option>
      </select>

        <h2>Editoras</h2>
      <select name="select">
        <option value=""></option>
        <option value="">Aleph</option>
        <option value="">Suma</option>
        <option value="">Editora Intrínseca</option>
        <option value="">Grupo Editorial Record"</option>
        <option value="">Editora Rocco</option>
        <option value="">Globo Livros</option>
        <option value="">Darkside Books</option>
        <option value="">Compainha de Letras</option>
      </select>

      

  <form>
    <div>
        <h2>Nome do Autor(a)</h2><input type="text" value="" placeholder="Nome do Autor(a)">
    </div>
  </form>


         <h2>Cadastrar Nome Do Livro </h2>
    
    </div>
      <br> <br>
    </div>
         
    <div class="form-input">
      <input type="text" v-model="novo_livro" />
      <button @click="salvar">Cadastrar</button>

      
    </div>
    <div class="list-times">
      <table>
        <thead> 
          <tr>
            <th>Livros cadastrados </th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="livros in livros" :key="livros.id">
            
            <td>{{ livros.nome }}</td>
            
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style>

.title {
  margin-top: 2rem;
  display: flex;
  justify-content: center;
  color: rgb(66, 66, 138);
}
.form-input {
  margin-top: 10px;
  display: flex;
  justify-content: center;
  color: blueviolet;
}

.form-input input {
  width: 60%;
  height: 40px;
  border: 1px solid rgb(199, 17, 17);
  border-radius: 10px;
  padding: 0 10px;
}

.form-input button {
  margin-left: 1%;
  width: 20%;
  height: 40px;
  border: 1px solid rgb(36, 127, 65);
  border-radius: 10px;
  background-color: rgb(36, 127, 65);
  color: white;
  font-weight: bold;
  cursor: pointer;
}

.list-times {
  display: flex;
  justify-content: center;
  
}

table {
  width: 50%;
  margin: 2% auto;
  border-collapse: collapse;
  color: rgb(82, 82, 134);
}

table tr th {
  border: 1px solid rgb(88, 60, 60);
  padding: 10px;
  font-weight: bold;
}

table tr td {
  border: 1px solid rgb(228, 8, 8);
  padding: 10px;
}

table tr {
  background-color: rgb(116, 7, 7) ;
}

body {
  background-color: black;
}


</style>
