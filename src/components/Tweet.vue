<template>
    <div class="tweet">
        <!-- <img :src="props.image" class="profile" alt="profile" /> -->
        <ProfileImage :image="props.image" />

        <div class="body">
            <div class="top">
                <!-- PREGUNTAR QUE ONDA USER DATA -->
                <User :name="props.name" :handle="props.handle"/>
                <!-- <span class="user">
                    <span class="name">{{props.name}}</span>
                    <span class="handle">{{props.handle}}</span>
                </span> -->
               
                <Timestamp :timestampPrueba="props.timestamp" />
                <!-- <span class="timestamp">{{props.timestamp}}</span> -->
            </div>


            <Message :message="props.message" />
            <!-- <p class="message">
                {{props.message}}
            </p> -->

            <Actions />
            <!-- <div class="actions"> -->
                <!-- Font Awesome icons -->
                <!-- <i class="far fa-comment"></i>
                <i class="fas fa-retweet"></i>
                <i class="far fa-heart"></i>
                <i class="fas fa-share"></i> -->
            <!-- </div> -->
        </div>

        <i class="fas fa-ellipsis-h"></i>
    </div>
</template>
  
<style scoped>
a {
    color: #42b983;
}
</style>


<script setup>
import { defineProps } from 'vue';
import ProfileImage from './ProfileImage.vue'; 
import User from './User.vue';
import Timestamp from './Timestamp.vue'; 
import Message from './Message.vue';
import Actions from './Actions.vue';

const props = defineProps (['name','image', 'handle', 'timestamp', 'message'])
</script>
