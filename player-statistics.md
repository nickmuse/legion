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
        }
      });
      
  });</script>
  
</head>
<body style="margin-left:0px">
<select id="search-year" name="year">
  <option></option>
  <option>2020</option>
  <option>2019</option>
</select>
<table id="stats" class="display responsive nowrap" style="width:100%">
    <thead>
      <th>Name</th>
      <th>Year</th>
      <th>Rec</th>
      <th>TD</th>
      <th>Comp</th>
      <th>PTD</th>
      <th>W/GP</th>
    </thead>
    <tbody>
      <tr>
        <td>Shoe</td>
        <td>2020</td>
        <td>9</td>
        <td>3</td>
        <td>0</td>
        <td>0</td>
        <td>1/2</td>
      </tr>
      <tr>
        <td>Shoe</td>
        <td>2019</td>
        <td>9</td>
        <td>3</td>
        <td>0</td>
        <td>0</td>
        <td>2/2</td>
      </tr>
      <tr>
        <td>Holmes</td>
        <td>2020</td>
        <td>11</td>
        <td>5</td>
        <td>0</td>
        <td>0</td>
        <td>2/2</td>
      </tr>
      <tr>
        <td>Holmes</td>
        <td>2019</td>
        <td>10</td>
        <td>6</td>
        <td>0</td>
        <td>6</td>
        <td>1/2</td>
      </tr>
    </tbody>
</table>
</body>
