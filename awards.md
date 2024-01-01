---
layout: page
title: Trophies, Awards and Inductions
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
	row += '<td>' + record.year + '</td>';
	row += '<td><a href="/awards.html?queries[search]=' + record.award + '&sorts[year]=-1">' + record.award + '</a></td>';
	row += '<td><a href="/awards.html?queries[search]=' + record.recipient + '&sorts[year]=-1">' + record.recipient + '</a></td>';
    row += '</tr>';
	return row;
	}
  
      $('#awards').dynatable({
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
          records: {{site.data.awards | jsonify}}
        }
      });
      
  });</script>
  
</head>

<div align="right">
Year: 
<select id="search-year" name="year">
  <option></option>
  <option>2021-2022</option><option>2020-2021</option>
  <option>2019-2020</option><option>2018-2019</option><option>2017-2018</option><option>2016-2017</option>
  <option>2015-2016</option><option>2014-2015</option><option>2013-2014</option><option>2012-2013</option>
</select>
</div>

<table id="awards" class="display responsive nowrap" style="width:80%">
    <thead>
      <th>Year</th>
      <th>Award</th>
      <th>Recipient</th>
    </thead>
    <tbody>
    </tbody>
</table>
