<template>
    
    <div class = "row">

        <div class = "col s12">

        <div clas="row">

            <div class = "col s12 ">

                <div class="input-field col s12">

                    <input v-on:input="$emit('search-value',name)" style="border-radius:10px;background-color:white;"   placeholder="" id="first_name" type="text" class="validate" v-model="name">
                    <label for="first_name" class="black-text" style="padding-left:10px; padding-top:30px; font-size:20px;"><i class="material-icons">search</i>Find Customers...</label>
                            
                </div>

            </div>

        </div>
        
        <div class = "row">
        
            <div class = "col s4"></div>

            <div class = "col s8 left-align">

                <div class="input-field col s12">

                <select @change="$emit('choose-sort-type',sortType)" style="border-radius:10px; box-shadow:1px 1px 1px grey;"  class="browser-default" v-model="sortType">
                    
                    <option value="" disabled selected>Filter By Name (A-Z)</option>
                    <option  value="1">Name (A-Z)</option>
                    <option value="2">Name (Z-A)</option>

                </select>

                <label class="black-text" style="padding-left:5px;">Filter By Name (A-Z)</label>

                    </div>

                </div>

        </div>

        </div>

    </div>

</template>
<script>

export default{

    name:'SearchBar',
    data(){

        return{
            sortType:null,
            name:'',
        }

    },
    methods:{

        beginSearch(e){

            this.$emit('search-value',this.name)

        }

    },
    created(){

          var elems = document.querySelectorAll('select');
          var instances = M.FormSelect.init(elems, {});

    },
    methods:{

        submitSearch(e){

            this.$emit('choose-sort-type',sortType)

        }
       
    }
}
</script>
