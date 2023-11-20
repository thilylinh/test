<template>
    <div class="leaderboard">
        <h2 class="leaderboard--title">Leaderboard</h2>
        <div class="leaderboard--content">
            <div class="leaderboard--item" :class="{ 'active': item.order == 1 }" v-for="(item, index) in dataLeaderBoard"
                :key="index">
                <div class="leaderboard--item__infor">
                    <div class="first"><span class="number">{{ item.order }}.</span>
                        <p class="avatar"></p>
                    </div>
                    <p>{{ item.name }}</p>
                    <div><img src="@/public/images/star.png" /></div>
                </div>
                <div class="leaderboard--item__result">
                    <p class="result--item">{{ item.numberWin }}</p>
                    <p class="result--item">{{ item.minutePlay }}</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            dataLeaderBoard: [
                {
                    id: 1,
                    name: 'TheW',
                    order: 2,
                    numberWin: 36,
                    minutePlay: 9.32
                },
                {
                    id: 1,
                    order: 1,
                    name: 'Rio',
                    numberWin: 36,
                    minutePlay: 9.32
                },
                {
                    id: 1,
                    order: 3,
                    name: 'Black',
                    numberWin: 36,
                    minutePlay: 9.32
                },
                {
                    id: 1,
                    name: 'Queen',
                    order: 4,
                    numberWin: 36,
                    minutePlay: 9.32
                },
                {
                    id: 1,
                    name: 'Cute',
                    order: 5,
                    numberWin: 36,
                    minutePlay: 9.32
                }
            ]
        }
    },

}
</script>
<style lang="scss" scoped>
@import "@/public/scss/components/LeaderBoard.scss";
</style>
  