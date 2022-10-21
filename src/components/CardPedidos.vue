<template>
    <div>
<table class="table table-bordered bg-warning">
    <thead class="border">
    <tr>
      <th scope="col">Pedido</th>
      <th scope="col">Cliente</th>
      <th scope="col">Pão</th>
      <th scope="col">Carne</th>
      <th scope="col">Adicional</th>
      <th scoope="col">Processo</th>
      <th scope="col">Altera Processo</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="burger in burgues" :key="burger.id">
      <th scope="row" >{{burger.id}}</th>
      <td>{{burger.nome}}</td>
      <td> {{burger.pao}}</td>
      <td>{{burger.carne}}</td>
      <td><p v-for="(opcional, index) in burger.opcionais" :key="index">{{opcional}}</p></td>
      <td>{{burger.status}}</td>
        <div class="select">
            <select name="" id="select">
                <option v-for="(statu, index) in status" :key="index">{{statu.tipo}}</option>
            </select>
      
        </div>

    </tr>
    
    
  </tbody>
</table>
    </div>    
</template>

<script>
export default {
    data() {
        return {
            burgues: null,
            msg: null,
            status: [],
        };
    },
    methods: {
      async getPedidos() {
            const req = await fetch("http://localhost:3000/burgues");
            const data = await req.json();
            this.burgues = data;
            console.log(this.burgues)
        },
        async getStatus() {
             const req = await fetch("http://localhost:3000/status");
             const data = await req.json();
             this.status = data;

        }
        
    },
    mounted() {
       this.getPedidos()
       this.getStatus()
    }
}
</script>

<style scoped>
    .table{
        border-radius: 18px;
        
        
    }
    .border{
        border-radius: 40px;
        background: #000;
        color: aliceblue;       
    }
    p{
        display: inherit;
        padding: 2px;

    }
    #select{
        margin: 8px auto;

         margin-left: 5px;

        
        margin-bottom: 0px;
         
        border: #000;
        height: 60px;
        border-radius: 20px;
    
    }
    .select{
        width: auto;
        border-top:  1px solid white;
    }
</style>
