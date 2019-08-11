# Webpack 4 for Vuejs
The configuration on this project have been separate on three parts. 
- Common configurations
- Development 
- Production 

In other projects also exist an staging phase to review and last check before production deployment, but in our case the previous steps are enough.

It's most important before develop an building strategies know how many technologies are involve on the project and how are the minimum requirement for theirs.

In this case we use the next frameworks:

1. Vue
    1. Vuex
    2. Vue-router
2. Buefy
    1. Bulma

#### Vue / Vuex / Vue-router
For Vue is important to prefetch and preload the chunks of css and js generate by webpack, because the Vue instance must be executed before load html by the web navigator.
The instances of vuex and vue-router are initialized out and before of the main instance of Vue, and later injected by parameter on the Vue instance. 

This behaviour force us to prefetch and preload the script on a certain order.

#### Buefy :love: Bulma
Bulma is a CSS framework and Buefy makes some libraries styled by bulma and provide some customization options for our components. For use this component the Vue instance needs to know where are theirs. These components are located in node_modules, one important point.