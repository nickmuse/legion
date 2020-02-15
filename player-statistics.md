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
  
  <script>
    $(document).ready(function() {
      $('#stats')
        .dynatable({
          features:{
            paginate: false,
            search: true,
            recordCount: false,
            perPageSelect: false
          }
        });
    });
  </script>
</head>
<body style="margin-left:0px">
<table id="stats" class="display responsive nowrap" style="width:100%">
    <thead>
      <th>Name</th>
      <th>Year</th>
      <th>Rec</th>
      <th>TD</th>
      <th>Comp</th>
      <th>PTD</th>
      <th>GP/W</th>
    </thead>
    <tbody>
    </tbody>
</table>
</body>
