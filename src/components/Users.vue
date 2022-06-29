<template>
  <div class="users">
    <h1>Users</h1>
    <canvas id="myChart" width="350" height="80"></canvas>
    </div>
</template>
<script>
    import Chart from 'chart.js/auto';
    export default{
        mounted(){
            console.log("Hello")
            const ctx = document.getElementById('myChart');
            const myChart = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: [ '','Jan4', '', 'Jan8','', 'Jan12','', 'Jan16','', 'Jan20','','Jan24','', '', 'Jan28','' ],
                    datasets: [ 
                                { 
                                    label:'Current Month',
                                    data: [4, 5.5, 5, 3, 4.5, 5, 6, 5, 5.5, 4, 3, 2.5, 4, 3.5,5], 
                                    backgroundColor: '#009bd5'
                                }, 
                                {
                                    label:'Past Month',
                                    data: [2, 1.2, 2, 1.5, 1.5, 1.5, 2, 1, 1,2.5, 2, 1.5, 1, 1.5,2], 
                                    backgroundColor: '#adbad6'
                                }
                            ]
                },
                options: {
                    scales: {
                        y: {
                            beginAtZero: true
                        }
                    }
                }
            });
            myChart;
        }
    }
</script>
<style>
    .users{
        height: 250px;
        background-color: white;
        border-radius: 10px;
        padding:20px;
        width:95%;
        margin: auto;
    }
    h1{
        font-size: 16px;
    }
</style>