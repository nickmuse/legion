---
layout: page
title: Player Statistics
sidebar_link: true
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
  
      $('#stats').dynatable({
        features:{
          paginate: false,
          search: true,
          recordCount: false,
          perPageSelect: false
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
Year: 
<select id="search-year" name="year">
  <option></option>
  <option>2020</option><option>2019</option><option>2018</option><option>2017</option>
  <option>2016</option><option>2015</option><option>2014</option><option>2013</option>
</select>
</div>

<table id="stats" class="display responsive nowrap" style="width:100%">
    <thead>
      <th>Name</th>
      <th>Year</th>
      <th>Rec</th>
      <th>TD</th>
      <th>Comp</th>
      <th>PTD</th>
      <th>W</th>
    </thead>
    <tbody>
    </tbody>
</table>
