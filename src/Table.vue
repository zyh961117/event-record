<template>
    <div class="table">
        <div class="table-hd">
            <a>＜</a>
            <span class="date">2018-10月-17日</span>
            <a>></a>
        </div>
        <table class="table-bd" cellspacing="0" cellpadding="0">
            <tr>
                <th></th>
                <th>10 <span class="am-pm">AM</span></th>
                <th>11 <span class="am-pm">AM</span></th>
                <th>12 <span class="am-pm">PM</span></th>
                <th>1 <span class="am-pm">PM</span></th>
                <th>2 <span class="am-pm">PM</span></th>
                <th>3 <span class="am-pm">PM</span></th>
                <th>4 <span class="am-pm">PM</span></th>
                <th>5 <span class="am-pm">PM</span></th>
                <th>6 <span class="am-pm">PM</span></th>
                <th>7 <span class="am-pm">PM</span></th>
                <th>8 <span class="am-pm">PM</span></th>
            </tr>
            <tr v-for="count in 4" :key="count">
                <td>1111111111</td>
                <td v-for="num in 11" :key="num">
                    <div class="hour">
                        <div class="half-hour-1"></div>
                        <div class="half-hour-2"></div>
                    </div>
                </td>
            </tr>
        </table>
    </div>
</template>

<script>
export default {}
</script>

<style lang="less" scoped>
.table {
    background-color: rgb(74, 48, 99);
}
.table-hd {
    height: 50px;
    line-height: 50px;
    color: antiquewhite;
    padding-left: 50px; 
    .date {
        padding: 0 20px;
    }
}
.table-bd {
    width: 100%;
    tr {
        th {
            width: 8%;
            color: antiquewhite;
            padding: 10px 0;
            border-left: 1px solid black;
            &:first-child {
                width: 12%;
            }
            .am-pm {
                font-size: 10px;
                font-weight: lighter;
            }
        }
        td{
            &:first-child {
                display: block;
                text-align: center;
                color: antiquewhite;
                line-height: 50px;
                border: none;
            }
            height: 50px;
            line-height: 0;
            border-left: 1px solid black;
            .hour {
                display: flex;
                height: 100%;
                .half-hour-1 {
                    width: 50%;
                    border-right: 1px solid black;
                }
                .half-hour-2 {
                    width: 50%;
                    border-left: 1px solid black;
                }
            }
        }
    }
}
</style>