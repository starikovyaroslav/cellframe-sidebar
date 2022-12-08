<template>
  <section class="search">
    <form class="search__form" v-on:submit.prevent>
      <div class="search__container">
        <div class="search__wrapper">
          <img class="search__icon" src="/SearchIcon.svg" alt="search-icon"/>
          <input
            placeholder="Search"
            maxLength="40"
            class="search__input"
            type="text"
            id="searchInput"
            name="searchInput"
            autoComplete="off"
          />
        </div>
        <span class="border-line"></span>
      </div>
    </form>
  </section>
</template>

<script>
export default {
  name: "Search"
}
</script>
