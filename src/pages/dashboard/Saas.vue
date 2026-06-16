<script setup lang="ts">
import Footer from "@/components/Footer.vue";
import Widgets from "@/sections/saas/Widgets.vue";
import Analytics from "@/sections/saas/Analytics.vue";
import TotalSpend from "@/sections/saas/TotalSpend.vue";
import RecentOrders from "@/sections/saas/RecentOrders.vue";
import TopSellingProducts from "@/sections/saas/TopSellingProducts.vue";
import { Button } from "@/components/ui/button";

function handleBotonPrueba() {
  alert("¡Botón de prueba funcionando!");
}
</script>

<template>
  <div class="grid grid-cols-12 mt-2 mb-6 gap-7">
    <!-- Botón de prueba -->
    <div class="col-span-12 flex justify-start">
      <Button @click="handleBotonPrueba" color="success">Botón de Prueba</Button>
    </div>

    <!-- Widget Cards -->
    <Widgets />

    <!-- Total Spend Graph -->
    <TotalSpend />

    <!-- Analytics Graph -->
    <Analytics />

    <!-- Recent Orders Table -->
    <RecentOrders />

    <!-- Top Selling Product List -->
    <TopSellingProducts />

    <!-- Footer -->
    <Footer></Footer>
  </div>
</template>
