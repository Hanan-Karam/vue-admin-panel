<template>
    <div class="canvas">
        <div class="heading">
            <h3>Viewers</h3>
            <h4>Last Week</h4>
        </div>
        <canvas id="lineChart" width="500" height="210"></canvas>
    </div>
</template>
<script>
    import Chart from 'chart.js/auto';
    export default{
        mounted(){
            console.log("Hello")
            const ctx = document.getElementById('lineChart');
            const labels = ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat'];
            const data = {
            labels: labels,
            datasets: [{
                label: 'Toggle Views',
                data: [ 10, 20, 10, 30, 20, 10, 25],
                fill: false,
                borderColor: "#009bd5",
                tension: 0.4, 
                // radius: 6 
            }],
            };
            const myChart = new Chart(ctx, {
                    type: 'line',
                    data: data,
                    options: {
                    legend: {
                        display: false
                    },
                }
            });
            myChart;
        }
    }
</script>
<style>
    .canvas{
        height: 90%;
        width: 65%;
        background-color: white;
        border-radius: 10px;
        padding:20px
    }
</style>