<script>
import theform from '../components/theform.vue'

export default{
    components : {
        theform
    }
}
</script>

<template>
    <div id="contact">
        <h1 class="title">Say Hello !</h1>
        <div class="contact-box">
            <div class="contact-left">
                <h3>Send me a message</h3>
                <theform/>
            </div>
            <div class="contact-right">
                <h3>Contact Info</h3>

                <table>
                    <tr>
                        <td>Email</td>
                        <td>hardydesigns@studio</td>
                    </tr>
                    <tr>
                        <td>Phone</td>
                        <td>123 456 7890</td>
                    </tr>
                    <tr>
                        <td>Address</td>
                        <td>Hardy Designs<br>
                            123 St,<br>Geelong 3216.
                        </td>
                    </tr>
                </table>
            </div>
        </div>
    </div>
</template>

<style>
#contact{
    width: 80%;
    margin: 50px auto;
}

.contact-box{
    background-color: white;
    display: flex;
    border-radius: 50px;
    box-shadow: 10px 10px 5px rgb(195, 195, 195);
}

.contact-left{
    flex-basis: 60%;
    padding: 40px 60px
}
.contact-right{
    flex-basis: 40% ;
    padding: 40px;
    border-radius: 0 50px 50px 0;
    background: black;
    color: white;
}

.form-row{
    display: flex;
    justify-content: space-between;
    margin-bottom: 20px;
}

.form-row,.form-group{
    flex-basis: 45%;
}

input{
    width: 100%;
    border: none;
    border-bottom: 1px solid black;
    outline: none;
    padding-bottom: 5px;
}

.text{
    width: 100%;
    border: 1px solid #ccc;
    outline: none;
    padding: 10px;
    box-sizing: border-box;
}

label{
    margin-bottom: 6px;
    display: block;
}

button{
    background: black;
    width: 100px;
    border: none;
    color: white;
    height: 35px;
    border-radius: 30px;
    margin-top: 20px;
}

.contact-left h3{
    margin-bottom: 30px;
}

.contact-right h3{
    margin-bottom: 30px;
}

tr td:first-child{
    padding-right: 20px;
}

tr td{
    padding-top: 30px;
}
</style>