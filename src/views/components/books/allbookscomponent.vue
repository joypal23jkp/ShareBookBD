<template>
   <div class="booklist-section w-100 mx-5 py-5">
         <div class="container py-0 pb-5">
             <div class="search-bar my-5">
                 <input type="text" class="form-control px-5" placeholder="Search Book Here......"
                 style="border-radius: 45px; color: black">
             </div>
             <hr>
            <div class="row row-grid justify-content-between align-items-center">
                <div class="col-lg-4 col-sm-10" v-for="item in booklist" :key="item">
                    <card class="border-0" hover shadow body-classes="py-5">
                        <icon name="ni ni-check-bold" type="primary" rounded class="mb-4">
                        </icon>
                        <h6 class="text-primary text-uppercase">Novel</h6>
                        <p class="description mt-3">This is websites is giving you permission to add your own book type.</p>
                        <div>
                            <badge type="primary" rounded>design</badge>
                            <badge type="primary" rounded>system</badge>
                            <badge type="primary" rounded>creative</badge>
                        </div>
                        <base-button tag="a" href="#" type="primary" class="mt-4">
                            Learn more
                        </base-button>
                    </card>
                </div>
            </div>
            <div class="base-pagination py-5 w-25 m-auto">
                <base-pagination :page-count="10" v-model="pagination.danger"></base-pagination>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            booklist: [1,2,3,4,5,6,7,8,9],
            pagination:{
                danger: ''
            }

        }
    }
};
</script>
<style>
</style>
