<template>
    <form @submit="wyslany">
        <div class="formularz">
            <h1>Zamówienia</h1>
            <label>
                <span>Imie i nazwisko:</span>
                <input type="text" name="imienazwisko" id="imienazwisko" class="wpis" v-model="imie">

            </label>
            <label>
                <span>Email:</span>
                <input type="text" name="email" id="email" class="wpis" v-model="email" pattern=".+@.+" required>

            </label>
            <label v-if="sprawdz" class="alert">
                    <span style="color:red;">To nie jest email</span>
                </label>
            <label>
                <span>Produkt:</span>
                <select name="produkt" id="produkt" class="produkt" v-model="produkt">
                <option value="pralka">pralka</option>
                <option value="telewizor">telewizor</option>
                <option value="lodówka">lodówka</option>
                <option value="laptop">laptop</option>
                </select>
            </label>
            <label>
                <span>Ilosc:</span>
                <input type="number" name="ilosc" id="ilosc" class="wpis" v-model="ilosc">
            </label>
            <label>
                <span>Wiadomość:</span>
                <textarea name="wiadomosc" id="wiadomosc" cols="30" rows="10" v-model="wiadomosc" class="wiadomosc"></textarea>
                <button class="przycisk" >Zamów</button>
                
            </label>
            
        </div>
    </form>
</template>
<style>
@import '@/assets/styles/window.css';
</style>
<script>
export default{
    name:'window-app',
    props: {
        msg: String
    },
    data(){
        return{
            imie:'Piotr',
            email:'Greatcat@onet.pl',
            produkt:'',
            ilosc:1,
            wiadomosc:'',
            sprawdz:false
        }
    }
    ,
    methods:{
        wyslany(event){
            event.preventDefault();
            if(this.imie==""|| this.email=="" ||this.produkt=="" || this.ilosc==0 )this.sprawdz=true;
            else{
                this.sprawdz=false;
            console.log(`Wszystko działa panie ${this.imie}`);
            }
        }
        
    }
}
</script>