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

Statistics have no feelings. Is there something more going on under the hood of LOL? Let's analyze.

### Defining the Scope
- Sometimes the mighty fall. Sometimes players improve. For that reason, this data only includes last 3 years of Game Days.
- This was calculated to serve some utility going into this season. For that reason, this data only includes receivers that are active for 21-22.
- Games Played prodominantly as QB has been struck from the player's record here. GP is modified here to include only Games Played prodominantly as a receiver.

### The Data
(click the AVGs to sort by them)

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

### Shoe's Takeaways
- JJ is a serious contender for the GOAT. While the Neighborhood Roadies' system is a system that both over-utilizes its star players, and generates numbers through higher quantities of short plays; it stands to reason that JJ would likely thrive equally in a system with less sporatic execution.
- In the coming years, second round talent needs to be redefined if teams want to stay relevant. With the data becoming easier to parse, 
- It needs to be said that Delmonte's value as Running Back will win games.
- We'll never truly be able to 'rank' receivers. The obvious grain of salt to consider here is who was quarterbacking for recievers during their peak/worst performances. QBs can also over/under utilize receivers. These chemistries are certainly something to consider when building a team. This is where your sense should be factored in. There are players at all tiers of this chart that would be positioned higher if they were more tactfully utilized. In the right system, players like Dingo and Esco could elevate to third round talent. In the same light, players like Maca retain their position as second rounders because coaches know these stats don't represent his game day potential.
