<template>
    <div>
        <button @click="dayin">打 印</button>
    </div>
</template>

<script>
import exportExcel from './js-export-excel.js'
var option = {};
导出表格标题 // 
option.fileName="警情处理Excel文档"
导出表格数据 // 
option.datas = [{
        sheetData: [{
            index: '1',
            time: '2019-7-25',
            deviceId:'00000011',
            state:'0'
        }, {
            index: '2',
            time: '2019-7-15',
            deviceId:'0000025',
            state:'1'
        }],
        sheetName: '警情处理表格',
        sheetFilter: ['index', 'time','deviceId','state'],
        sheetHeader: ['序号', '时间','设备','状态'],
        columnWidths: [2, 6,4,2]
    },
];
实例化表格 // 
var toExcel = new exportExcel(option);
toExcel.saveExcel();
</script>
