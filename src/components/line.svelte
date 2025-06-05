<script>
    import { chart } from 'svelte-apexcharts';


    let options = {
        chart: {
            type: 'bar',
            height: 'auto'
        },
        series: [{
            name: 'Sales',
            data: [30, 40, 35, 50, 49, 60, 70, 91, 125]
        }],
        xaxis: {
            categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998, 1999]
        },
        plotOptions: {
            bar: {
                borderRadius: 4,
                columnWidth: '70%'
            }
        }
    };
</script>

<div class="chart-container">
    <div use:chart={options} />
</div>

<style>
    .chart-container {
        width: 100%;
        max-width: 800px;
        margin: 0 auto;
    }

    .chart-container > div {
        min-height: 300px;
    }
</style>