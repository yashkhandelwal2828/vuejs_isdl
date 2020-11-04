<template>
<b-card style="margin-top: 30px; height: 379.73px;">

    <b-img style="margin-top: -67px; box-shadow: 0 10px 30px -12px rgba(0,0,0,.42), 0 4px 25px 0 rgba(0,0,0,.12), 0 8px 10px -5px rgba(0,0,0,.2)" v-bind="mainProps" :src="cardUserImage" rounded="circle" alt="Circle image"></b-img>
    <b-card-body>
        <!-- <b-card-title style="text-align:center;"> -->
        <h6 style="text-align:center; color: #999999;">CEO / Co-Founder</h6>
        <!-- </b-card-title> -->
        <!-- <b-card-sub-title style="text-align:center;" class="mb-2"> -->
        <h4 style="text-align:center; color:0000DE;">Alec Thompson</h4>
        <!-- </b-card-sub-title> -->
        <b-card-text center style="text-align:center;">
            Don't be scared of the truth because we need to restart the human
            foundation in truth And I love you like Kanye loves Kanye I love Rick
            Owens’ bed design but the back is...
        </b-card-text>
    </b-card-body>
    <b-card-body class="mx-auto">
        <b-button center href="#" variant="success" style="color:white; border-radius:999px; padding:12px 30px;">FOLLOW</b-button>
    </b-card-body>

</b-card>
</template>

<script>
export default {
    name: "user-card",
    props: {
        cardUserImage: {
            type: String,
            default: require("@/assets/img/faces/marc.jpg")
        }
    },
    data() {
        return {
            mainProps: {
                width: 130,
                height: 130,
                center: true,
            }
        };
    }
};
</script>

<style></style>
