<script>
import CartItem from './CartItem.vue'
import NavBar from './NavBar.vue'

export default {
    data() {

        return {
            hotdog: "default",
            numDresses: 0,
            dict: {},
            index: 0,
        }
    },
    components: { NavBar, CartItem },
    methods: {
        addToCart(itemName) {
            if (this.dict[itemName] != undefined) {
                this.dict[itemName].count++;

            } else {
                this.dict[itemName] = { count: 0 }
            }
            this.index++;
        },
    }
}
</script>

<template>
    <header>
        <NavBar></NavBar>
    </header>
    <p class="myCart">

    </p>

    <body>
        <main>
            <li v-for="itemN in Object.keys(dict)">
                <strong>{{ itemN }} </strong>
                {{ dict[itemN]}}
            </li>

            <CartItem>

                <body>
                    <img alt="Cart Item" class="picture"
                        src="https://images.squarespace-cdn.com/content/v1/5dd8630d09ab5908e35b35a0/1627664408104-DFFG9X75O0MBIFBFGH0O/Ketchup+sticker.jpg"
                        width="250" height="250" />
                    <div>Disco Hotdog</div>
                    <p>Price: $100</p>
                    <p>Description: Amazing party dog</p>
                    <button v-on:click="addToCart('Disco Hotdog')">Add Item To Cart</button>
                </body>

            </CartItem>

            <CartItem>

                <body>
                    <img alt="Cart Item" class="picture" img
                        src="https://www.washingtonpost.com/resizer/D6V5TO35ggS_RU7kLijiFiHLO7s=/arc-anglerfish-washpost-prod-washpost/public/IPJAY7WQUAI6ZCDL353BQPJDH4.jpg"
                        width="250" height="250" />
                    <div>Food Hotdog</div>
                    <p>Price: $25</p>
                    <p>Description: Yummy hotdo with vegetables</p>
                    <button v-on:click="addToCart('Food Hotdog')">Add Item To Cart</button>
                </body>

            </CartItem>

            <CartItem>

                <body>
                    <img alt="Cart Item" class="picture"
                        src="https://img.freepik.com/free-vector/fast-food-sticker-design-with-hot-dog-isolated_1308-67129.jpg?w=2000&t=st=1678800288~exp=1678800888~hmac=cd1d59dbf99e6bc96dbac9ad74fa067151412cadd835b89b54eed5a2f7d16c6d"
                        width="250" height="250" />
                    <div>Cartoon Hotdog</div>
                    <p>Price: $5</p>
                    <p>Description: Cartoon hotdog sticker</p>
                    <button v-on:click="addToCart('Cartoon Hotdog')">Add Item To Cart</button>
                </body>
            </CartItem>

            <CartItem>

                <body>
                    <img alt="Cart Item" class="picture"
                        src="https://i.pinimg.com/originals/6a/14/de/6a14de48ce302cb067b08b47c35f832b.jpg" width="250"
                        height="250" />
                    <div>Dog Hotdog</div>
                    <p>Price: $1000</p>
                    <p>Description: A cute dog dressed in a hot dog costume</p>
                    <button v-on:click="addToCart('Dog Hotdog')">Add Item To Cart</button>
                </body>
        </CartItem>

    </main>


</body></template>

<style scoped></style>
