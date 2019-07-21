<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-container>
        <b-navbar-brand>
          <nuxt-link class="nav-brand" :to="{name: 'home'}">Мастер-класс ЕН</nuxt-link>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <li class="nav-item">
              <nuxt-link class="nav-link" :to="{name: 'catalog'}">Каталог</nuxt-link>
            </li>

            <li class="nav-item">
              <nuxt-link class="nav-link" :to="{name: 'catalog'}">О нас</nuxt-link>
            </li>

            <li class="nav-item">
              <nuxt-link class="nav-link" :to="{name: 'catalog'}">Контакты</nuxt-link>
            </li>

            <li class="nav-item">
              <nuxt-link class="nav-link" :to="{name: 'catalog'}">Корзина</nuxt-link>
            </li>


            <b-nav-item href="/catalog"></b-nav-item>


          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-form>
              <b-form-input size="sm" class="mr-sm-2" placeholder="Поиск"></b-form-input>
              <b-button size="sm" class="my-2 my-sm-0" type="submit">Поиск</b-button>
            </b-nav-form>

            <b-nav-item-dropdown text="Lang" right>
              <b-dropdown-item href="#">RU</b-dropdown-item>
              <b-dropdown-item href="#">UA</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown right>
              <!-- Using 'button-content' slot -->
              <template slot="button-content"><em>Личный кабинет</em></template>
              <b-dropdown-item href="#">Профиль</b-dropdown-item>
              <b-dropdown-item href="#">Войти</b-dropdown-item>
            </b-nav-item-dropdown>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
    <nuxt/>
  </div>

</template>

<style scoped>
  .nav-brand{
    color: rgba(255, 255, 255, 0.5);
  }
  .nav-brand:hover{
    color: rgba(255, 255, 255, 0.75);
  }
</style>
