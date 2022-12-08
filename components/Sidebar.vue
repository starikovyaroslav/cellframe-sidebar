<template>
  <section class="sidebar">
    <div class="sidebar__container">
      <nuxt-link class="sidebar__link-logo" no-prefetch exact to="/">
        <img class="sidebar__logo" src="/logo.svg" alt="logo">
      </nuxt-link>
      <div class="sidebar__wrapper">
        <ul class="sidebar__list">
          <li class="sidebar__links" v-for="(item, index) of menuItem" :key="index">
            <nuxt-link no-prefetch exact class="sidebar__link" active-class="active" :to="item.path">
              <img class="sidebar__link-icon" :src="item.icon" alt="icon"/>
              <p class="sidebar__link-text">{{ item.name }}</p>
            </nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: 'Sidebar',

  data() {
    return {
      menuItem: [
        {
          path: '/wallet',
          name: 'Wallet',
          icon: 'navigation/Wallet.svg'
        },
        {
          path: '/dex',
          name: 'DEX',
          icon: 'navigation/DEX.svg'
        },
        {
          path: '/tx-explorer',
          name: 'TX Explorer',
          icon: 'navigation/TX Explorer.svg'
        },
        {
          path: '/certificates',
          name: 'Certificates',
          icon: 'navigation/Certificates.svg'
        },
        {
          path: '/tokens',
          name: 'Tokens',
          icon: 'navigation/Tokens.svg'
        },
        {
          path: '/vpn-client',
          name: 'VPN Client',
          icon: 'navigation/VPN client.svg'
        },
        {
          path: '/vpn-service',
          name: 'VPN service',
          icon: 'navigation/VPN service.svg'
        },
        {
          path: '/console',
          name: 'Console',
          icon: 'navigation/Console.svg'
        },
        {
          path: '/logs',
          name: 'Logs',
          icon: 'navigation/Logs.svg'
        },
        {
          path: '/settings',
          name: 'Settings',
          icon: 'navigation/Settings.svg'
        },
        {
          path: '/dapps',
          name: 'dApps',
          icon: 'navigation/dApps.svg'
        }
      ]
    }
  }
}
</script>
