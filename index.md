## About Me

Born in Manchester, England, I'm now a junior at Lehigh University majoring in Finance, with a passion for data-driven decision-making and operational strategy. My experience spans both corporate and entrepreneurial environments, where I've built a versatile skill set in financial analysis, risk management, and business operations.

Currently, I'm interning at NexAmbit Marketing through the Lehigh@NasdaqCenter program, where I support business operations and strategic initiatives in a fast-paced, innovation-focused environment.

Previously, I worked at PKF O’Connor Davies as a Financial Services Advisory Intern, contributing to vendor due diligence processes by creating risk assessments, summarizing private equity firm financials, and identifying key mitigation steps to support client compliance and decision-making.

Beyond internships, I spent 7 years running a successful self-employed venture, generating over $20,000 in revenue through data-backed market research and resale strategies. I used automated tools to source inventory and Excel to analyze profitability, optimize pricing, and forecast performance trends.

I’m always eager to take on new challenges and explore opportunities at the intersection of finance, operations, and technology. Connect with me on linkedin!

---

## Portfolio

<!-- You can link to other websites, PDFs in this repo, and other pages in this repo -->

_**[Natural language processing 10-Ks to identify risks](midterm_summary)**_

You can show off your midterm analysis by moving the report components and output into this file. Or...

<img src="images/dummy_thumbnail.jpg?raw=true"/>

---

**[CEO Personalities](https://ceo-personalities.streamlit.app/)**

<h2>CEO Return Analysis</h2>
<table id="csv-table" class="display" style="width:100%">
    <thead></thead>
    <tbody></tbody>
</table>

<!-- Load jQuery and DataTables -->
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<link rel="stylesheet" href="https://cdn.datatables.net/1.13.6/css/jquery.dataTables.min.css"/>
<script src="https://cdn.datatables.net/1.13.6/js/jquery.dataTables.min.js"></script>

<script>
fetch('assets/ceo_return_analysis.csv')
  .then(response => response.text())
  .then(csv => {
    const rows = csv.trim().split('\n').map(row => row.split(','));
    const headers = rows.shift();

    const thead = document.querySelector('#csv-table thead');
    const tbody = document.querySelector('#csv-table tbody');

    // Set table headers
    thead.innerHTML = '<tr>' + headers.map(h => `<th>${h}</th>`).join('') + '</tr>';

    // Set table rows
    rows.forEach(row => {
      const tr = document.createElement('tr');
      row.forEach(cell => {
        const td = document.createElement('td');
        td.textContent = cell;
        tr.appendChild(td);
      });
      tbody.appendChild(tr);
    });

    // Initialize DataTable
    new DataTable('#csv-table');
  });
</script>

---

## Hobbies

Golf, MMA, Football (soccer), Lifting

---
<p style="font-size:11px">Page template forked from <a href="https://github.com/evanca/quick-portfolio">evanca</a></p>
<!-- Remove above link if you don't want to attibute -->
