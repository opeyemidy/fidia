<template>
  <nav>
    <div class="site-logo-wrapper">
      <span class="logo-icon">
        <company-icon />
      </span>
      <span class="store-title">Store name</span>
      <span>
        <chevron-icon />
      </span>
    </div>
    <div class="link-container">
      <nav-link to="/">
        <template #icon> <home-icon /> </template>
        Home
      </nav-link>
      <dropdown-link name="Payments">
        <template #icon> <payment-icon /> </template>
        <nav-link submenu to="/"> Reviews </nav-link>
        <nav-link submenu to="/"> Disputes </nav-link>
        <nav-link submenu to="/"> All transactions </nav-link>
        <nav-link submenu to="/"> Top-ups </nav-link>
        <nav-link submenu to="/"> Collected fees </nav-link>
        <nav-link submenu to="/"> Transfers </nav-link>
        <nav-link submenu to="/"> Payouts </nav-link>
      </dropdown-link>
      <div>
        <nav-link to="/">
          <template #icon> <balance-icon /> </template>
          Balances </nav-link
        ><nav-link to="/">
          <template #icon> <customer-icon /> </template>
          Customers </nav-link
        ><nav-link to="/">
          <template #icon> <connected-icon /></template>
          Connected accounts </nav-link
        ><nav-link to="/">
          <template #icon><products-icon /></template>
          Products </nav-link
        ><nav-link to="/">
          <template #icon> <reports-icon /> </template>
          Reports
        </nav-link>
      </div>

      <div class="mt-24">
        <nav-link to="/">
          <template #icon> <balance-icon /> </template>
          Developers </nav-link
        ><switch-button to="/">
          <template #icon> <checkbox /> </template>
          View test data </switch-button
        ><nav-link to="/">
          <template #icon> <settings-icon /> </template>
          Settings
        </nav-link>
      </div>
    </div>
  </nav>
</template>

<script>
import chevronIcon from './chevronIcon.vue'
import CompanyIcon from './companyIcon.vue'
import HomeIcon from './homeIcon.vue'
import NavLink from './navLink.vue'
import dropdownLink from './dropdownLink.vue'
import PaymentIcon from './paymentIcon.vue'
import ConnectedIcon from './connectedIcon.vue'
import ProductsIcon from './productsIcon.vue'
import ReportsIcon from './reportsIcon.vue'
import Checkbox from './Checkbox.vue'
export default {
  components: {
    chevronIcon,
    CompanyIcon,
    HomeIcon,
    PaymentIcon,
    NavLink,
    dropdownLink,
    ConnectedIcon,
    ProductsIcon,
    ReportsIcon,
    Checkbox,
  },
}
</script>
