<template>
  <section>
    <b-field label="Filtros">
      <b-field grouped>
        <b-select v-model="filtro.regional" placeholder="Regional" expanded>
          <option v-for="(regional, i) in regionais" :value="regional" :key="i">{{ regional }}</option>
        </b-select>
        <b-select v-model="filtro.empresa" placeholder="Empresa" expanded>
          <option v-for="(empresa, i) in empresas" :value="empresa" :key="i" >{{ empresa }}</option>
        </b-select>
        <b-select v-model="filtro.filial" placeholder="Filial" expanded>
          <option v-for="(filial, i) in filiais" :value="filial" :key="i" >{{ filial }}</option>
        </b-select>
        <b-select v-model="filtro.area" placeholder="Area" expanded>
          <option v-for="(area, i) in areas" :value="area" :key="i" >{{ area }}</option>
        </b-select>
      </b-field>
    </b-field>
    <b-table :data="data" :columns="columns"
            :selected.sync="vagaSelecionada" focusable></b-table>
  </section>
</template>

<script>
export default {
  name: 'Vagas',
  data () {
    return {
      vagaSelecionada: null,
      filtro: {
        regional: null,
        empresa: null,
        filial: null,
        area: null
      },
      regionais: ['Maranhão', 'Pará'],
      filiais: ['It Happens', 'Black Swan', 'Mateus Cohama', 'Mateus Centro Administrativo', 'Mateus Belém', 'Armazém Mateus 116'],
      empresas: ['Mateus Supermercados', 'Armazém Mateus', 'It Happens'],
      areas: ['Tecnologia da Informação', 'Recrutamento e Seleção', 'Operação Loja', 'Operação CDs'],
      data: [
        {
          id: 1,
          cargo: 'Programador Junior',
          filial: 'It Happens',
          date: '2016-10-15 13:43:27',
          cidade: 'São Luís',
          area: 'Tecnologia da Informação'
        },
        {
          id: 2,
          cargo: 'Açougueiro',
          filial: 'Mateus Cohama',
          date: '2016-12-15 06:00:53',
          cidade: 'São Luís',
          area: 'Operação Loja'
        },
        {
          id: 3,
          cargo: 'Analista de Recrutamento',
          filial: 'Mateus Centro Administrativo',
          date: '2016-04-26 06:26:28',
          cidade: 'São Luís',
          area: 'Recrutamento e Seleção'
        },
        {
          id: 4,
          cargo: 'Repositor Mercearia',
          filial: 'Mateus Belém',
          date: '2016-04-10 10:28:46',
          cidade: 'Belém',
          area: 'Operação Loja'
        },
        {
          id: 5,
          cargo: 'Repositor Aéreo',
          filial: 'Armazém Mateus 116',
          date: '2016-12-06 14:38:38',
          cidade: 'São Luís',
          area: 'Operação CDs'
        }
      ],
      columns: [
        { field: 'cargo', label: 'Vaga' },
        { field: 'filial', label: 'Filial' },
        { field: 'cidade', label: 'Cidade' },
        { field: 'area', label: 'Área' }
      ]
    }
  }
}
</script>
