<template>
    <div class="card">
        <div class="card-body">
            <div class="card-image">
                <img :src="course.card_img" alt="" />
            </div>
            <h2 class="card-category">{{ course.category }}</h2>
            <div class="card-content">

                <h2 class="card-heading">{{ course.heading }}</h2>
                <div class="card-students">{{ course.total_students }}</div>
                <div class="card-details">
                    <div class="card-time">{{ course.total_time }}</div>
                    <div class="card-lectures">{{ course.toatl_lectures }}</div>
                </div>
                <hr>
                <div class="card-author">
                    <div style="display: flex; align-items: center;">
                        <div class="card-author-avatar">
                            <img :src="course.avatar" alt="" />
                        </div>
                        <div class="card-author-info">
                            <div class="card-author-name">{{ course.course_by }}</div>
                        </div>
                    </div>
                    <div class="card-price">
                        <div class="card-fee">₹{{ course.fee }}</div>
                        <div class="card-fee-discounted">₹{{ course.fee_after_discount }}</div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>
  
<script>
import '@/styles/card.css'
export default {
    name: "Card",
    props: {
        course: Object,
    },
};
</script>
  