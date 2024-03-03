<script>
    import axios from 'axios';

    export default {
    name: "ContactUsView",
    data() {
        return {
            name: '',
            email: '',
            message: ''
        }
    },
    methods: {
        
        sendEmail() {
            axios.post('http://127.0.0.1:8000/api/contact-us', {
                name: this.name,
                email: this.email,
                message: this.message
            })
            .then((response) => {
                console.log(response);
                this.resetForm();
            })
            .catch(function (error) {
                console.log(error);
            })
            .finally(function () {
                // always executed
            });
        },
        resetForm() {
            this.name = '';
            this.email = '';
            this.message = '';
        }
    }
    }
</script>

<template>
    <div class="container mt-3">
        <div class="row justify-content-center ">
            <div class="col-12">
                <h1 class="text-center">
                    Contact Us
                </h1>
            </div>
            <div class="col-10">
                <form @submit.prevent="sendEmail">
                    <div class="mb-3">
                        <label for="name" class="form-label">Name</label>
                        <input type="text" class="form-control" id="name" v-model="name">
                    </div>
                    <div class="mb-3">
                        <label for="email" class="form-label">Email</label>
                        <input type="email" class="form-control" id="email" v-model="email">
                    </div>
                    <div class="mb-3">
                        <label for="message" class="form-label">Message</label>
                        <textarea class="form-control" id="message" rows="5" v-model="message"></textarea>
                    </div>
                    <div class="mb-3">
                        <button type="submit" class="btn btn-primary">Send</button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>