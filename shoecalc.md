---
layout: page
title: Shoe's Calculations
sidebar_link: false
---

<head>
  <link rel="stylesheet" href="https://cdn.datatables.net/1.10.20/css/jquery.dataTables.min.css">
  <link rel="stylesheet" href="jquery.dynatable.css">
  <!-- <link rel="stylesheet" href="https://cdn.datatables.net/1.10.20/css/jquery.dataTables.responsive.min.css"> -->
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
  <script src="https://cdn.datatables.net/1.10.20/js/jquery.dataTables.min.js"></script>
  <!-- <script src="https://cdn.datatables.net/1.10.20/js/jquery.dataTables.responsive.min.js"></script> -->
  <script src="jquery.dynatable.js"></script>

  <script>$(document).ready(function() {
  
    function custom_writer(rowIndex, record, columns, cellWriter) {
	row = '<tr>';
	row += '<td>' + record.name + '</td>';
	row += '<td>' + record.gp + '</td>';
        row += '<td>' + record.rec + '</td>';
	row += '<td>' + record.rectd + '</td>';
        row += '<td>' + record.rtd + '</td>';
        row += '<td>' + record.avgrec + '</td>';
	row += '<td>' + record.avgrectd + '</td>';
        row += '<td>' + record.avgrtd + '</td>';
        row += '</tr>';
	return row;
	}
  
      $('#advanced').dynatable({
        features:{
          paginate: false,
          search: false,
          recordCount: false,
          perPageSelect: false
        },
	writers: {
		_rowWriter: custom_writer
	},
        dataset: {
          records: {{site.data.advanced | jsonify}}
        }
      });
      
  });</script>
  
</head>

<table id="advanced" class="display responsive nowrap" style="width:80%">
    <thead>
      <th>Name</th>
      <th>GP</th>
      <th>REC</th>
      <th>RECTD</th>
      <th>RTD</th>
      <th>AVG REC</th>
      <th>AVG RECTD</th>
      <th>AVG RTD</th>
    </thead>
    <tbody>
    </tbody>
</table>
