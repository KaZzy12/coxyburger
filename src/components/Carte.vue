<template>
    <div class="section" id="carte">
        <h2>Carte</h2>
        <div>
            <ul class="menu">
                <li>
                    <router-link class="nav-link" :to="{name: 'BrowseFrites'}">
                        Frites
                    </router-link>
                </li>
                <li>
                    <router-link class="nav-link" :to="{name: 'BrowseHamburgers'}">
                        Hamburgers
                    </router-link>
                </li>
                <li>
                    <router-link class="nav-link" :to="{name: 'Browsemitraillettes'}">
                        Mitraillettes
                    </router-link>
                </li>
                <li>
                    <router-link class="nav-link" :to="{name: 'BrowseBrochettes'}">
                        Brochettes
                    </router-link>
                </li>
                <li>
                    <router-link class="nav-link" :to="{name: 'BrowseSnacks'}">
                        Snacks
                    </router-link>
                </li>
                <li>
                    <router-link class="nav-link" :to="{name: 'BrowsePetiteRestauration'}">
                        Petite restauration
                    </router-link>
                </li>
                <li>
                    <router-link class="nav-link" :to="{name: 'BrowseSauces'}">
                        Sauces
                    </router-link>
                </li>
                <li>
                    <router-link class="nav-link" :to="{name: 'BrowseVegetarien'}">
                        Végétarien
                    </router-link>
                </li>
                <li>
                    <router-link class="nav-link" :to="{name: 'BrowseSofts'}">
                        Softs
                    </router-link>
                </li>
                <li>
                    <router-link class="nav-link" :to="{name: 'BrowseAlcools'}">
                        Bières/Vin
                    </router-link>
                </li>
            </ul>
        </div>
        <router-view v-if="$route.matched.length"></router-view>
    </div>
</template>

<script>
export default {
  name: 'BrowseMenu',
};
</script>

<style>
.menu {
  display: flex;
  justify-content: space-around;
  margin: 0 100px;
  font-size: 20px;
}
ul {
  list-style-type: none;
}
.nav-link {
  text-decoration: none;
  color: inherit;
}
.router-link-active {
  color: red;
}
</style>
