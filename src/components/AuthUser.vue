<template>
    <pre>{{ this.isLoggedIn }}</pre>
    <div class="container">
        <div class="row">
            <div class="col-md-6">
                <div class="card">
                    <div class="card-body">
                        <div v-if="isLoggedIn">
                            <p class="h3 fw-bold text-success">Welcome User</p>
                            <p class='fst-italic'>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Delectus nihil optio quod. Dicta, quidem voluptatibus.</p>
                        </div>
                        <div v-if="!isLoggedIn">
                            <p class="h3 fw-bold text-danger">Thank You !!</p>
                            <p class='fst-italic'>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Delectus nihil optio quod. Dicta, quidem voluptatibus.</p>
                        </div>
                        <div>
                            <button v-if="!isLoggedIn" class="btn btn-success btn-sm m-1" @click="login()">Login</button>
                            <button v-if="isLoggedIn" class="btn btn-danger btn-sm m-1" @click="logout()">Logout</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AuthUser',
    data: function(){
        return{
            isLoggedIn: false
        };
    },
    methods: {
        login : function(){
            this.isLoggedIn = true;
        },
        logout : function(){
            this.isLoggedIn = false;
        }
    }
};
</script>