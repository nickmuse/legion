---
layout: page
title: Player Statistics
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
	row += '<td><a href="/players.html?queries[search]=' + record.name + '&sorts[year]=-1">' + record.name + '</a></td>';
	row += '<td>' + record.year + '</td>';
	row += '<td>' + record.gp + '</td>';
        row += '<td>' + record.rec + '</td>';
	row += '<td>' + record.rectd + '</td>';
        row += '<td>' + record.rtd + '</td>';
        row += '<td>' + record.ptd + '</td>';
        row += '<td>' + record.int + '</td>';
	row += '<td>' + record.sac + '</td>';
	row += '<td>' + record.deftd + '</td>';
        row += '</tr>';
	return row;
	}
  
      $('#stats').dynatable({
        features:{
          paginate: false,
          search: true,
          recordCount: false,
          perPageSelect: false
        },
	writers: {
		_rowWriter: custom_writer
	},
        inputs: {
          queries: $('#search-year')
        },
        dataset: {
          records: {{site.data.stats | jsonify}}
        }
      });
      
  });</script>
  
</head>

<div align="right">
Per Game Average <input type="checkbox" id="avg" name="avg" value="Average Per Game">
</div>

<div align="right">
Year: 
<select id="search-year" name="year">
  <option></option>
  <option>2021</option>
  <option>2020</option><option>2019</option><option>2018</option><option>2017</option>
  <option>2016</option><option>2015</option><option>2014</option><option>2013</option>
</select>
</div>

<table id="stats" class="display responsive nowrap" style="width:80%">
    <thead>
      <th>Name</th>
      <th>Year</th>
      <th>GP</th>
      <th>REC</th>
      <th>RECTD</th>
      <th>RTD</th>
      <th>PTD</th>
      <th>INT</th>
      <th>SAC</th>
      <th>DEFTD</th>
    </thead>
    <tbody>
    </tbody>
</table>
