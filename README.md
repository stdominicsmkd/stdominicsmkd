<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kids Fest Results</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #e0f7fa;
            color: #333;
            margin: 0;
            padding: 20px;
            font-size: 20px;
        }
        h1 {
            font-size: 3em;
            color: #4A90E2;
            text-align: center;
            margin: 20px;
        }
        h2 {
            color: #00796b;
            margin-top: 20px;
        }
        .category {
            background-color: #ffffff;
            border: 2px solid #4db6ac;
            border-radius: 10px;
            padding: 15px;
            margin: 10px auto;
            width: 80%;
            text-align: center;
        }
        button {
            background-color: #00796b;
            color: white;
            border: none;
            border-radius: 5px;
            padding: 10px 20px;
            cursor: pointer;
            font-size: 16px;
            margin: 10px;
        }
        button:hover {
            background-color: #004d40;
        }
        table {
            width: 80%;
            margin: 40px auto;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #4db6ac;
            padding: 8px;
            text-align: center;
        }
        th {
            background-color: #00796b;
            color: white;
        }
    </style>
</head>

<body>
<h1><em>TALENTIA 2024</em></h1>

<div class="category">
    <h2>Results</h2>
    <button onclick="showCategory('Category 1')">Category 1</button><br>
    <button onclick="showCategory('Category 2')">Category 2</button><br>
    <button onclick="showCategory('School Wise')">School Wise Results</button><br>
</div>

<div id="results" class="category" style="display:none;">
    <h2 id="result-title"></h2>
    <div id="result-content"></div>
</div>

<footer style="text-align: center; margin-top: 20px;">
    <p>Thank you for participating in the Kids Fest</p>
</footer>

<script>
    function showCategory(category) {
        const resultTitle = document.getElementById('result-title');
        const resultContent = document.getElementById('result-content');
        const resultsDiv = document.getElementById('results');
        resultContent.innerHTML = ''; // Clear previous content

        if (category === 'Category 1') {
            resultTitle.textContent = 'Category 1';
            resultContent.innerHTML = `
                <button onclick="showItem('Stage Items 1')">Stage Item</button>
                <button onclick="showItem('Off Stage Item 1')">Off Stage Item</button>
                <button onclick="showItem('Group Item 1')">Group Item</button>
            `;
        } else if (category === 'Category 2') {
            resultTitle.textContent = 'Category 2';
            resultContent.innerHTML = `
                <button onclick="showItem('Stage Items 2')">Stage Item</button>
                <button onclick="showItem('Off Stage Item 2')">Off Stage Item</button>
                <button onclick="showItem('Group Item 2')">Group Item</button>
            `;
        } else if (category === 'School Wise') {
            resultTitle.textContent = 'School Wise Results';
            resultContent.innerHTML = `
                <table>
                    <tr>
                        <th>Sl. No</th>
                        <th>School Name</th>
                        <th>Category 1</th>
                        <th>Category 2</th>
                        <th>Total Points</th>
                    </tr>
                    <tr>
                        <td>1</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>2</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>3</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
                    </tr>
<tr>
                        <td>4</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>5</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>6</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
                    </tr>
<tr>
                        <td>7</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
                    </tr>
                    <tr>
                        <td>8</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
                    </tr>
                </table>
            `;
        }

        resultsDiv.style.display = 'block';
    }

    function showItem(item) {
        const resultContent = document.getElementById('result-content');
        resultContent.innerHTML = ''; // Clear previous content

        const itemButtons = {
            'Stage Items 1': `
                <h3>Stage Items</h3>
                <button onclick="displayContent('Action Song (English)')">Action Song (English)</button>
                    <button onclick="displayContent('Action Song (Malayalam)')">Action Song (Malayalam)</button>
                    <button onclick="displayContent('Story Telling (English)')">Story Telling (English)</button>
                    <button onclick="displayContent('Story Telling (Malayalam)')">Story Telling (Malayalam)</button>
                    <button onclick="displayContent('Recitation (Malayalam)')">Recitation (Malayalam)</button>
                    <button onclick="displayContent('Recitation (English)')">Recitation (English)</button>
                    <button onclick="displayContent('Folk Dance')">Folk Dance</button>
                    <button onclick="displayContent('Single Dance')">Single Dance</button>
                    <button onclick="displayContent('Fancy Dress')">Fancy Dress</button>
                    <button onclick="displayContent('Smart Kid')">Smart Kid</button>
                    <button onclick="showCategory('Category 1')">Back</button
            `,
            'Stage Items 2': `
                <h3>Stage Items</h3>
                <button onclick="displayContent('ELOCUTION (English)')">ELOCUTION (English)</button>
                    <button onclick="displayContent('ELOCUTION (Malayalam)')">ELOCUTION (Malayalam)</button>
                    <button onclick="displayContent('RECITATION (Malayalam)')">RECITATION (Malayalam)</button>
                    <button onclick="displayContent('RECITATION (English)')">RECITATION (English)</button>
                    <button onclick="displayContent('FOLK DANCE')">FOLK DANCE</button>
                    <button onclick="displayContent('SINGLE DANCE')">SINGLE DANCE</button>
                    <button onclick="displayContent('FANCY DRESS')">FANCY DRESS</button>
                    <button onclick="displayContent('SMART KID')">SMART KID</button>
                    <button onclick="showCategory('Category 2')"> Back</button>
            `,
            'Off Stage Item 1': `
                <h3>Off Stage Items</h3>
                <button onclick="displayContent('Pencil Drawing')">Pencil Drawing</button>
                    <button onclick="displayContent('Painting Crayon')">Painting Crayon</button>
                    <button onclick="displayContent('Clay Modeling')">Clay Modeling</button>
                    <button onclick="displayContent('Memory Retention')">Memory Retention</button>
                    <button onclick="showCategory('Category 1')"> Back</button>
            `,
            'Off Stage Item 2': `
                <h3>Off Stage Items</h3>
                <button onclick="displayContent('SPELLING MARATHON')">SPELLING MARATHON</button>
                    <button onclick="displayContent('PENCIL DRAWING')">PENCIL DRAWING</button>
                    <button onclick="displayContent('PAINTING CRAYON')">PAINTING CRAYON</button>
                    <button onclick="displayContent('CLAY MODELING')">CLAY MODELING</button>
                    <button onclick="displayContent('MEMORY RETENTION')">MEMORY RETENTION</button>
                    <button onclick="showCategory('Category 2')"> Back</button>
            `,
            'Group Item 1': `
                <h3>Group Items</h3>
               <button onclick="displayContent('Oppana')">Oppana</button>
                    <button onclick="displayContent('Western Dance')">Western Dance</button>
                    <button onclick="displayContent('Thiruvathira')">Thiruvathira</button>
                    <button onclick="showCategory('Category 1')"> Back</button>
            `,
            'Group Item 2': `
                <h3>Group Items</h3>
                 <button onclick="displayContent('GROUP DANCE')">GROUP DANCE</button>
                    <button onclick="displayContent('OPPANA ')">OPPANA </button>
                    <button onclick="displayContent('RECORDED COMEDY SKIT')">RECORDED COMEDY SKIT</button>
                    <button onclick="displayContent('THIRUVATHIRA')">THIRUVATHIRA</button>
                    <button onclick="showCategory('Category 2')"> Back</button>
            `
        };

        resultContent.innerHTML = itemButtons[item] || '<p>No items available.</p>';
    }

    function displayContent(item) {
        const resultContent = document.getElementById('result-content');
        const itemTables = {
            'Action Song (English)': `
               Action Song(English) <table> 
<tr>
   <th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th></tr>
 <tr>
                        <td>1</td> 
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>

                </table>

            `,
            'Action Song (Malayalam)': `
              Action Song(Malayalam)  <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>

                       
                </table>
            `,
'Story Telling (English)': `
               Story Telling(English) <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> l</td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 

                       
                </table>
            `,
'Story Telling (Malayalam)': `
          Story Telling(Malayalam)      <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>    
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>

                       
                </table>
            `,
'Recitation (Malayalam)': `
           Recitation(Malayalam)     <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 
                       
                </table>
            `,
'Recitation (English)': `
       Recitation(English)         <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 

                       
                </table>
            `,
'Folk Dance': `
        Folk Dance        <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>11</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>

                       
                </table>
            `,
'Single Dance': `
        Single Dance        <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td>101</td>
                        <td> AAA</td>
                        <td> SSSS</td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 
                       
                </table>
            `,
'Fancy Dress': `
           Fancy  dress    <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>11</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr><tr>
                        <td>12</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>

                       
                </table>
            `,
'Smart Kid': `
            Smart Kid    <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 

                       
                </table>
            `,
'ELOCUTION (Malayalam)': `
       Elocution(Malayalam)         <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 

                       
                </table>
            `,

            // Add more items as needed
            'ELOCUTION (English)': `
          Elocution(English)      <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>

                       
                </table>
            `,
'RECITATION (English)': `
            Recitation(English)    <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 

                       
                </table>
            `,
'RECITATION (Malayalam)': `
          Recitation(Malayalam)      <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>11</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr><tr>
                        <td>102</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>13</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>

                       
                </table>
            `,
'FOLK DANCE': `
            Folk Dance    <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>

                       
                </table>
            `,
'SINGLE DANCE': `
         Single Dance       <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 

                       
                </table>
            `,
'FANCY DRESS': `
            Fancy Dress    <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>11</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>

                       
                </table>
            `,
'SMART KID': `
          Smart Kid      <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 

                       
                </table>
            `,
'Pencil Drawing': `
         Pencil Drawing       <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
                       
                </table>
            `,
'Painting Crayon': `
         Painting Crayon       <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td></td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>11</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>

                       
                </table>
            `,
'Clay Modeling': `
         Clay Modeling       <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 

                       
                </table>
            `,
'Memory Retention': `
             Memory Retention   <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 
                       
                </table>
            `,
'PENCIL DRAWING': `
           Pencil Drawing     <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 

                       
                </table>
            `,
'PAINTING CRAYON': `
    Painting Crayon            <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>10</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>11</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
<tr>
                        <td>12</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
                       
                </table>
            `,
'CLAY MODELING': `
             Clay Modeling   <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 
                       
                </table>
            `,
'MEMORY RETENTION': `
        Memory Retention        <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
                       
                </table>
            `,
'SPELLING MARATHON': `
         Spelling Marathon       <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>6</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>7</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>8</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>9</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 
                       
                </table>
            `,
'Oppana': `
        Oppana        <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
                       
                </table>
            `,
'Thiruvathira': `
          Thiruvathira      <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 
                       
                </table>
            `,
'Western Dance': `
            Western Dance    <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td></td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>5</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 
                       
                </table>
            `,

'GROUP DANCE': `
        Group Dance        <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
                       
                </table>
            `,
'OPPANA ': `
            Oppana    <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>4</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 
                       
                </table>
            `,
'THIRUVATHIRA': `
         Thiruvathira       <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 
                       
                </table>
            `,
'RECORDED COMEDY SKIT': `
              Recorded Comedy Skit  <table>
                    <tr>
<th>Sl. No</th>
                        <th>Chest No</th>
                        <th>Name</th>
                        <th>School</th>
                        <th>Place</th>
                        <th> Grade</th>
                        <th>Point</th>
</tr>

 <tr>
                        <td>1</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr>
 <tr>
                        <td>2</td>
                        <td></td>
                        <td> </td>
                        <td> </td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> <tr>
                        <td>3</td>
                        <td></td>
                        <td> </td>
                        <td></td>
                        <td></td>
 <td></td>
                        <td></td>
                    </tr> 
                       
                </table>
            `,


            // Continue for other items...
        };

        resultContent.innerHTML = itemTables[item] || '<p>No results available for this item.</p>';
    }
</script>
</body>
</html>

