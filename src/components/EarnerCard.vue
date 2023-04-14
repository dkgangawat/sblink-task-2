<template>
    <div class="Earner-card">
        <div class="Earner-card-image">
            <img :src="cardData.img" alt="Card image" />
        </div>
        <div class="Earner-card-earning">₹{{ cardData.earning }}</div>
    </div>
</template>
  
<script>
export default {
    name: "EarnerCard",
    props: {
        cardData: Object,
    },
};
</script>
  
  