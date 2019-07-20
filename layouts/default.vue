<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="primary">
      <b-container>
        <b-navbar-brand>
          <nuxt-link :to="{name: 'home'}">Мастер-класс ЕН</nuxt-link>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <nuxt-link :to="{name: 'catalog'}">Каталог</nuxt-link>
            <b-nav-item href="/catalog"></b-nav-item>
            <b-nav-item href="#">Контакты</b-nav-item>
            <b-nav-item href="#">О нас</b-nav-item>
            <b-nav-item href="#">Корзина</b-nav-item>

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

