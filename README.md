Download Link: https://assignmentchef.com/product/solved-cis1300-assignment-4-conways-game-of-life
<br>
<h1>Description</h1>




The <em>Game of Life</em> consists of a two-dimension grid of <em>cells</em>.  Each cell is either <em>alive</em> or <em>dead</em>. Each cell has eight <em><u>neighbours</u></em>, which are the cells that are horizontally, vertically, or diagonally adjacent.

<table width="234">

 <tbody>

  <tr>

   <td width="78">X-1, Y-1</td>

   <td width="78">X-1, Y</td>

   <td width="78">X-1, Y+1</td>

  </tr>

  <tr>

   <td width="78">X, Y-1</td>

   <td width="78">X,Y</td>

   <td width="78">X, Y+1</td>

  </tr>

  <tr>

   <td width="78">X+1, Y-1</td>

   <td width="78">X+1, Y</td>

   <td width="78">X+1, Y+1</td>

  </tr>

 </tbody>

</table>







At each step in time (or <em>tick</em>), the following transitions occur:

<ol>

 <li>Any <strong>live</strong> cell with <strong>fewer than two</strong> <strong>live</strong> neighbours <strong>dies</strong>, as if by underpopulation.</li>

 <li>Any <strong>live</strong> cell with <strong>two or three</strong> <strong>live</strong> neighbours <strong>lives</strong> on to the next generation.</li>

 <li>Any <strong>live</strong> cell with <strong>more than three</strong> <strong>live</strong> neighbours <strong>dies</strong>, as if by overpopulation.</li>

 <li>Any <strong>dead</strong> cell with <strong>exactly three</strong> <strong>live</strong> neighbours becomes a <strong>live</strong> cell, as if by reproduction.</li>

</ol>




The initial pattern constitutes the <em>seed</em> of the system. The first generation is created by applying the above rules simultaneously to every cell in the seed; births and deaths occur simultaneously.




<h1>Reference</h1>

<u>https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life</u>




<strong>Now you have the description of the game but how do you program it? </strong>




<strong>Step 1.</strong>  Write code to read in the seed (initial) grid.

<ul>

 <li>Set the size of your grid as #define statements (or you can make them dynamic – see the end of the assignment for more information).</li>

 <li>Open a file whose name is given as argv[1].</li>

 <li>Each line in the file will be a row in the grid and each number on the line represents a cell (or column) in the grid, e.g. if your grid was 4 X 4 then the following could be a seed:</li>

</ul>

0 0 0 0

0 1 1 0

0 1 1 0

0 0 0 0

<ul>

 <li>Read these values into a 2-D array. The grid can be an integer array or a character array and the values can be 1’s and 0’s (input format) or ‘X’s and spaces (display format).</li>

</ul>










<strong>Step 2.</strong>  Write code to display the grid.

<ul>

 <li>Using the 2-D array populated by the previous code. Designate a live cell by an X and a dead cell by a space.</li>

</ul>







<ul>

 <li>Notice that there is a frame around the grid and in the lower right corner will be a number representing the tick (number of times that the grid has been evaluated).</li>

 <li>To see if your code is working for both reading and writing the grid, a number of seed files will be supplied with the assignment. These files will have the extension .seed.</li>

</ul>




<strong>Step 3.</strong>  Evaluate all of the cells in the grid to see if there are alive or dead in the next tick.

<ul>

 <li>Since all of the cell calculations are happening “simultaneously” you need to have two arrays. One 2-D array represents the “world” (grid) as it is now and one represents the world after the calculations have been made.</li>

</ul>







<h1>Tick 0 (Seed) – Current Grid (for 1<sup>st</sup> tick)</h1>




<table width="269">

 <tbody>

  <tr>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54">X</td>

   <td width="54"></td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54">X</td>

   <td width="54">X</td>

   <td width="54">X</td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

  </tr>

 </tbody>

</table>




<h1>Tick 1 – Future Grid (for 1<sup>st</sup> tick) and Current Grid (for 2<sup>nd</sup> tick)</h1>




<table width="269">

 <tbody>

  <tr>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54">X</td>

   <td width="54">X</td>

   <td width="54">X</td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54">X</td>

   <td width="54">X</td>

   <td width="54">X</td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54">X</td>

   <td width="54"></td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

  </tr>

 </tbody>

</table>




<h1>Tick 2 – Future Grid (for 2<sup>nd</sup> tick) and Current Grid (for 3<sup>rd</sup> tick)</h1>




<table width="269">

 <tbody>

  <tr>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54">X</td>

   <td width="54"></td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54">X</td>

   <td width="54"></td>

   <td width="54">X</td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54">X</td>

   <td width="54">X</td>

   <td width="54">X</td>

   <td width="54"></td>

  </tr>

  <tr>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

   <td width="54"></td>

  </tr>

 </tbody>

</table>




<ul>

 <li>In other words, evaluate a cell in the “Current” grid/array and put its new value (after applying Rules 1, 2, 3, or 4) in a “Future” grid/array. After displaying the “Future” grid/array, it becomes the “Current” grid/array.</li>

</ul>

<h1>Other Considerations</h1>




<ol>

 <li>How can you simulate the grid changing over time but remaining in the same space on the screen?

  <ul>

   <li>Before you display the grid, you need to “clear” the screen. This clears all text off the screen and returns the cursor to the top of the screen.  The C code to do this is: system(“clear”);</li>

  </ul></li>

</ol>




<ol start="2">

 <li>How can you stop each successive drawing of the grid from coming too quickly to the screen?

  <ul>

   <li>After each display of the grid, you need to have the system “sleep” before it displays the next generation of grid. The C code to do this is: system ( “sleep 0.25” );</li>

  </ul></li>

</ol>




<ol start="3">

 <li>After loading the seed, you should let the user see it before the process starts so as the user the following question:</li>

</ol>

Start? (y or n):

If the user answers n then terminate the program.




<ol start="4">

 <li>How many ticks should the program display?

  <ul>

   <li>Well it is hard to know what the seed will do so we should establish a number of ticks that will be displayed and then as the user if they want to continue with another set of ticks. The set of ticks will be the 2<sup>nd</sup> parameter on the command line.  If this is missing then the number is set to 50.  The program will go for either atoi(argv[2]) ticks or 50 ticks before asking: Continue? (y or n): and then doing either another set of ticks or terminating the program.</li>

  </ul></li>

</ol>




<ol start="5">

 <li>Where is the seed file entered?

  <ul>

   <li>The name of the seed file is the 1<sup>st</sup> command line parameter (argv[1]).</li>

  </ul></li>

</ol>




<ol start="6">

 <li>What do I do when I get to the edge of the world?

  <ul>

   <li>At the edges of the grid, do not consider cells that are “not” in the world (ignore them when calculating the new world).</li>

  </ul></li>

</ol>




<ol start="7">

 <li>What size (dimensions) should I make the world?

  <ul>

   <li>Please make your world 20 rows by 40 columns.</li>

   <li>But what if I want to make this dynamic (set as a command line parameter). You will get 2 bonus marks (2 full marks on your final grade).</li>

  </ul></li>

</ol>




<ol start="8">

 <li>Do I need to use functions?

  <ul>

   <li>No but they would be nice J</li>

  </ul></li>

</ol>




<ol start="9">

 <li>What should I do if the grid/world does not change from one tick to the next?

  <ul>

   <li>If that happens (and it does) you should terminate the program.</li>

  </ul></li>

</ol>

<h1>Example Command Lines</h1>




$ ./cgol diehard.seed 20

<ul>

 <li>Seed file is named diehard.seed</li>

 <li>The time interval (number of ticks) is 20.</li>

</ul>




$ ./cgol R-pentomino.seed

<ul>

 <li>Seed file is named R-pentomino.seed</li>

 <li>The time interval (number of ticks) is 50.</li>

</ul>