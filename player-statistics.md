---
layout: page
title: Player Statistics
sidebar_link: true
---

<head>
  <link rel="stylesheet" href="https://cdn.datatables.net/1.10.20/css/jquery.dataTables.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
  <script src="https://cdn.datatables.net/1.10.20/js/jquery.dataTables.min.js"></script>
  <script>
    $(document).ready(function(){
      $('#stats').DataTable({
        paging: false;
        responsive: true;
      });
    });
  </script>
</head>
  
<table id="stats" class="display" style="width:100%">
    <thead>
        <tr>
            <th>Name</th>
            <th>Wins</th>
            <th>Rec</th>
            <th>TD</th>
            <th>Comp</th>
            <th>PTD</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Frank</td>
            <td>6</td>
            <td>2</td>
            <td>1</td>
            <td>27</td>
            <td>11</td>
        </tr>
        <tr>
            <td>Justin</td>
            <td>4</td>
            <td>18</td>
            <td>9</td>
            <td>1</td>
            <td>0</td>
        </tr>
    </tbody>
</table>
