<template>
    
    <div class="container mt-3">
        <div v-if="loading">
            <Spinner/>
        </div>
        <div class="row" v-if="!loading && Object.keys(user).length > 0">
            <div class="col">
                <pre>{{ user }}</pre>
            </div>
        </div>
        <div class="row">
            <div class="col">
                <router-link class="btn btn-success ms-3" to="/users">Back</router-link>
            </div>
        </div>
    </div>
</template>

<script>
import { UserService } from '@/services/UserService';
import { Spinner } from '@/components/Spinner';
export default {
    components: { Spinner },
    name: 'UserDetails',
    data: function(){
        return {
            loading: false,
            user: {},
            errorMessage: null
        }
    },
    created: async function(){
        let userId = this.$route.params.userId;
        console.log(userId);
        try {
            this.loading = true;
            let response = await UserService.getUser(userId);
            this.user = response.data;
            this.loading = false;
            console.log(this.user);
        //     console.log(user);
        } catch (error) {
            this.loading = false;
            this.errorMessage = error;
            // console.log(error);
        }
    }
}
</script>

<style scoped>

</style>