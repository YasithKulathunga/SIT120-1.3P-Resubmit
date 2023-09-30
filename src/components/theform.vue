<script>
export default{
    data(){
        return{
            name:'',
            mobile:0,
            email: '',
            address:'',
            message:'',
        }
    }
}

</script>

<template>
    <form>
                    <div class="form-row">
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input v-model="name" placeholder="Richard Smith">
                        </div>
                        <div class="form-group">
                            <label for="Phone">Phone</label>
                            <input v-model.number="mobile" placeholder="0123 456 789">
                        </div>
                    </div>
                    <div class="form-row">
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input v-model="email" placeholder="richardsmith@email.com">
                        </div>
                        <div class="form-group">
                            <label for="address">Address</label>
                            <input v-model="address" placeholder="123 st, Geelong 3216">
                        </div>
                    </div>
                    <label for="message">Message</label>
                    <textarea class="text" v-model="message" rows="5" placeholder="Your Message"></textarea>

                    <button>Submit</button>
        </form>
</template>