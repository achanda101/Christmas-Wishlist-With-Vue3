<template>
<div>
   <h1>My Holiday Gift Wishlist</h1> 
   <input type="text" v-model="filterText">
   <p>{{ filteredWishlist }}</p>
   <ul v-bind:class="$style.wishlist">
       <li v-bind:key="gift.id" v-for="gift in gifts">
           <h3>{{ gift.label }}</h3>
           <img v-bind:src="`images/${gift.image}`" v-bind:alt="gift.label" />
           <div>
                <p>Votes: {{ gift.votes }}</p>
                <button>Wish for this</button>
           </div>
       </li>
   </ul>
</div>
</template>

<script>
import gifts from "../../public/data";
export default {
    data: () => ({
        gifts,
        filterText: '',
    }),
    computed: {
        filteredWishlist: function() {
            return this.filterText + ' boop ';   
        }    
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<!-- "scoped" does not fully protect you from side-effects/conflicts when you have commonly-used names -->
<!-- Add "module" attribute to truly limit CSS to this component only -->
<!-- Need to add v-bind to class wishlist and $style. -->
<!-- Right-click and inspect the rendered page and you will see this component's name appended to the class name -->

<style lang="scss" module>
    ul.wishlist {
        list-style: none;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    
        li {
            padding: 10px;
            flex-basis: 30%;
            border: 1px dotted #eeeeee;
            display: flex;
            flex-direction: column;
            justify-content: space-between;

            img {
                width: 200px;
                align-self: center;
            }
        }
    }
    
</style>
