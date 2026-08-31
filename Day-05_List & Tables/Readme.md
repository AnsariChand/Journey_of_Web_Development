# LIst & Tables
(ul, ol, li, table, thead, tbody, tr, th, td, colspan, rowspan)

- Unordered List
- Ordered List
- Description List

## Unordered List
~~~
<ul>      
 <li>Tea Patti</li>
 <li>Milk</li>
 <li>Sugar</li>
 <li>Buscuits</li>
 <li>Kurkure</li>
</ul>
~~~

## Unordered List attributes
- Disc
- None
- square
- Circle

## Ordered List
~~~
    <h2>Ordered List</h2>
    <h2>Ordered List & His Typo of Attributes</h2>
        <ol type="A">
            <li>Boil the water</li>
            <li>take sugar and chai patti</li>
            <li>Take milk</li>
            <li>Boil for two mins</li>
        </ol>

        <ol type="a">
            <li>Boil the water</li>
            <li>take sugar and chai patti</li>
            <li>Take milk</li>
            <li>Boil for two mins</li>
        </ol>

        <ol type="1">
            <li>Boil the water</li>
            <li>take sugar and chai patti</li>
            <li>Take milk</li>
            <li>Boil for two mins</li>
        </ol>

        <ol type="I">
            <li>Boil the water</li>
            <li>take sugar and chai patti</li>
            <li>Take milk</li>
            <li>Boil for two mins</li>
        </ol>

        <ol type="i">
            <li>Boil the water</li>
            <li>take sugar and chai patti</li>
            <li>Take milk</li>
            <li>Boil for two mins</li>
        </ol>

        <ol start="5">
            <li>Boil the water</li>
            <li>take sugar and chai patti</li>
            <li>Take milk</li>
            <li>Boil for two mins</li>
        </ol>
~~~

## Description List
~~~
<h1>Description list</h1>
        <dl>
            <dt>Terms and Conditions</dt>
            <dd>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum aperiam dignissimos quia!
            </dd>
        </dl>
~~~

## Nested List
~~~
<h2>Nested List</h2>
        <ol>
            <li>Fruits
                <ol>
                <li>Apple</li>
                <li>Cherry</li>
                <li>Mango</li>
                </ol>
            </li>
            <li>Vegetables
                <ol>
                    <li>Cabbage</li>
                    <li>Capsicum
                        <ul type="disc">
                            <li>Pink Capsicum</li>
                            <li>Brown Capsicum</li>
                            <li>Green Capsicum</li>
                        </ul>
                    </li>
                </ol>
            </li>
            
        </ol>
~~~

## Tables
A Table is Collection of Row and Column.

- tr  Table row for creating a Table row.
- td  Table Data for Create a data in the table
 ~~~
 <div>
        <h1>Tables</h1>
        <table>
            <tr>
                <td>1</td>
                <td>2</td>
            </tr>

            <tr>
                <td>3</td>
                <td>4</td>
            </tr>
        </table>

        <h2>Students Score</h2>
        <table>
            <tr>
                <td>Students Subject</td>
                <td>Maths</td>
                <td>Hindi</td>
                <td>English</td>
                <td>Science</td>
            </tr>
            <tr>
                <td>Anu</td>
                <td>90</td>
                <td>59</td>
                <td>70</td>
                <td>96</td>
            </tr>
            <tr>
                <td>Sumit</td>
                <td>60</td>
                <td>36</td>
                <td>97</td>
                <td>85</td>
            </tr>
            <tr>
                <td>Ayan</td>
                <td>60</td>
                <td>36</td>
                <td>45</td>
                <td>50</td>
            </tr>
            <tr>
                <td>Sumit</td>
                <td>60</td>
                <td>55</td>
                <td>79</td>
                <td>85</td>
            </tr>
        </table>

    </div>
 ~~~

 ## RowSpan and Colspan
 merging data cells with rowspan and colspan

 ~~~
 <div>
        <h2>Rowspan and Colspan</h2>
        <table>
            <tr>
                <td rowspan="2"></td>
                <td colspan="2 ">Average</td>
                <td rowspan="2">Red Eyes</td>
            </tr>
            <tr>
                <td>height</td>
                <td>weight</td>
            </tr>
            <tr>
                <td>Males</td>
                <td>1.9</td>
                <td>3.003</td>
                <td>40%</td>
            </tr>
            <tr>
                <td>Females</td>
                <td>1.7</td>
                <td>0.002</td>
                <td>43%</td>
            </tr>
            <caption>A test Table with merge cells</caption>
        </table>
    </div>
 ~~~

