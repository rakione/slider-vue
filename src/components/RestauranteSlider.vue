<template>
    <div class="back-slider">
        <div class="container-slider">
            <div class="container">
                <div class="row">
                    <div class="col-12 slider-frame" :class="{active: element.active}"  v-for="(element,index) in arreglo" v-bind:key="index" >
                        <h1 class="title-slider text-center">{{ element.title }}</h1>
                        <p class="text-container text-center">{{ element.text }}</p>
                    </div>
                    <button class="btn btn-primary btn-follow" @click="next()" >next()</button>
                </div>
            </div>
        </div>
    </div>
</template>
<script>

export default {
    name: 'RestauranteSlider',
    props: {
        
    },
    data() {
        return {
            index: 0,
            arreglo: [
                {
                    title: 'Restaurante',
                    text: 'El mejor restaurante de la ciudad',
                    active: true
                },
                {
                    title: 'Restaurante 1',
                    text: 'Calidad',
                    active: false

                },
                {
                    title: 'Restaurante 2',
                    text: 'El mejor',
                    active: false
                }
            ]
        }
    },
    methods: {
        next() {
            let step = true;
            this.arreglo.forEach( (element,index)  => {
                if (element.active && step) {
                    element.active = false;
                    if (index === this.arreglo.length - 1) {
                        this.arreglo[0].active = true;
                    } else {
                        this.arreglo[index + 1].active = true;
                    }
                    step = false;
                }
                
            });
        }
    },
    mounted() {
        this.timer = setInterval(() => {
            this.next();
        }, 2000);
    },

}


</script>
<style>
.container-slider {
    height: 600px;
    width: 100%;
    /* background:url(https://www.ikusi.com/mx/wp-content/uploads/sites/2/2022/06/post_thumbnail-4efabca9bd56b38edc0058c4ba006481.jpeg); */
}
.slider-frame {
    display: none;
}
.slider-frame.active {
    display: block;
}
h1.title-slider.text-center {
    color: #fff;
    margin: 200px 0px 50px 0px;
    font-size: 4rem;
    font-weight: 600;
}
p.text-container.text-center {
    color: #fff;
    font-size: 2rem;
    font-weight: 300;

}
</style>