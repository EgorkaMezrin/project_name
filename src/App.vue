<template>
    <div class="app">
        <post-form
        @create="createPost"
        />
        <post-list 
        :posts="posts"
        
    />
        
    </div>
</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";
export default{
    components:{
        PostList,
        PostForm,
    },
    data(){
        return{
            posts:[
                {id: 1, title:'JavaScript', body:'описание поста'},
                {id: 2, title:'JavaScript 2', body:'описание поста 2'},
                {id: 3, title:'JavaScript 3', body:'описание поста 3'},

            ],
        }
    },
    methods: {
        createPost(post, second, third){
            console.log(post);
            console.log(second);
            console.log(third);


            


        },
       
    }
}

</script>

<style>
*{
    margin:0;
    padding:0;
    box-sizing: border-box;
}
.app{
    padding: 20px;

}



</style>