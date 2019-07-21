<template>
  <b-form>
    <b-form-group label="Тип материала:">
    <b-form-select v-model="selectedMaterial_type" :options="material_type"></b-form-select>
    </b-form-group>
    <b-form-group label="Материал:">
    <b-form-select v-model="selectedMaterial" :options="material"></b-form-select>
    </b-form-group>
    <b-form-group label="Форма:">
    <b-form-select v-model="selectedShape" :options="shape"></b-form-select>
    </b-form-group>
  </b-form>
</template>

<script>
  export default {
    name: "CatalogFilter",
    data() {
      return {
        selectedMaterial_type: null,
        material_type: [
          { value: 'Натуральные камни', text: 'Натуральные камни' },
          { value: 'Синтетические камни', text: 'Синтетические камни' },
          { value: null, text: 'Все' }
        ],
        selectedMaterial: null,
        material: [
          { value: 'Раух-топаз', text: 'Раух-топаз' },
          { value: 'Стекло ювелирное', text: 'Стекло ювелирное' },
          { value: 'Топаз', text: 'Топаз' },
          { value: 'Фианит', text: 'Фианит' },
          { value: 'Изумруд', text: 'Изумруд' },
          { value: 'Турмалин', text: 'Турмалин' },
          { value: 'Аквамарин', text: 'Аквамарин' },
          { value: null, text: 'Все' }
        ],
        selectedShape: null,
        shape: [
          { value: 'Маркиз', text: 'Маркиз' },
          { value: 'Овал', text: 'Овал' },
          { value: 'Октагон', text: 'Октагон' },
          { value: 'Багет', text: 'Багет' },
          { value: 'Круг', text: 'Круг' },
          { value: 'Сердце', text: 'Сердце' },
          { value: 'Фантазийный', text: 'Фантазийный' },
          { value: 'Триллион', text: 'Триллион' },
          { value: null, text: 'Все' }
        ],

      }
    }
  }
</script>

<style scoped>

</style>
