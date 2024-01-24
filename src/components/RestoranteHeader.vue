<template>
    <header class="header">
        <div class="container">
            <div class="row">
                <div class="col-12 col-lg-4">
                    <img src="image/logo.png" class="logo" alt="logo"/>
                </div>
                <div class="col-5 no-display">
                    <nav>
                        <div class="row justify-content-end">
                            <div class="col-2">
                                <router-link class="item-menu" to="/">Home</router-link> 
                            </div>
                            <div class="col-2">
                                <router-link class="item-menu" to="/lisisng">Lising</router-link> 
                            </div>
                            <div class="col-2">
                                <router-link class="item-menu" to="/blog">Blog</router-link> 
                            </div>
                            <div class="col-2">
                                <router-link class="item-menu" to="/page">Page</router-link>
                            </div>
                            <div class="col-2">
                                <router-link class="item-menu" to="/singin">
                                    <span class="user-login"><font-awesome-icon icon="fa-solid fa-user" /></span>
                                    Signin</router-link>
                            </div>
                            <div class="col-2">
                                <router-link class="item-menu" to="/register">
                                    <span class="user-login"><font-awesome-icon icon="fa-solid fa-user-plus" /></span>
                                    Register</router-link>
                            </div>
                        </div>
                    </nav>
                </div>
                <div class="col-3">
                    <div class="row justify-content-center">
                        <div class="col">
                            <button class="btn btn-lg add-listing">Add Listing</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>
<script>

</script>
<style>
.header{
    height: 90px;
    widows: 100%;
    background-color: #ffffff;
}
img.logo {
    width: 187px;
    height: 46px;   
    margin: 22px auto 22px auto;
    position: relative;
    display: block;
}
.no-display {
    display: none;
}
button.btn.btn-lg.add-listing {
    width: 200px;
    height: 45px;
    margin: 22px auto 22px auto;
    position: relative;
    display: block;
    background: #e8280b;
    color: #fff;
    border-radius: 25px;
    padding: 0px;
}

.item-menu {
    color: #2c3e50;
    text-decoration: none;
    font-size: 1.0rem;
    text-align: center;
    top: 30px;
    position: relative;
}

a.router-link-active.router-link-exact-active.item-menu {
    text-decoration-color: #eb200b;
    text-decoration-line: underline;
    text-underline-offset: 11px;
}
.user-login svg {
    height: 13px;
    position: absolute;
    left: -19px;
    top: 3px;
}

@media (min-width: 720px) {
    .no-display {
        display: block;
    }
    img.logo {
        margin-top: 22px;
        margin-left: 5px;
        margin-bottom: auto;
        margin-right: auto;

    } 
}


</style>