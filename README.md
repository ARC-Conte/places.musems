<html>
    <head>
        <title>musems | fun places</title>
        <style>
                       /* Style the search box */
                       #mySearch {
            width: 100%;
            font-size: 18px;
            padding: 11px;
            border: 1px solid #ddd;
            }
            /* Style the navigation menu */
            #myMenu {
            list-style-type: none;
            padding: 0;
            margin: 0;
            }
            /* Style the navigation links */
            #myMenu li a {
            padding: 12px;
            text-decoration: none;
            color: black;
            display: block
            }
            #myMenu li a:hover {
            background-color: #eee;
            }
            * {
            box-sizing: border-box;
            }
            #myInput {
            background-image: url('/css/searchicon.png');
            background-position: 10px 12px;
            background-repeat: no-repeat;
            width: 100%;
            font-size: 16px;
            padding: 12px 20px 12px 40px;
            border: 1px solid #ddd;
            margin-bottom: 12px;
            }
            #myUL {
            background-color: rgb(114, 114, 114);
            list-style-type: none;
            padding: 0;
            margin: 0;
            }
            #myUL li a {
            border: 1px solid #ddd;
            margin-top: -1px; /* Prevent double borders */
            background-color: rgb(143, 143, 143);
            padding: 12px;
            text-decoration: none;
            font-size: 18px;
            color: black;
            display: block
            }
            #myUL li a:hover:not(.header) {
                background-color: rgb(83, 83, 83);
                color: white;
            }
            body{
                background-color: rgb(177,177,177);
            }            
        </style>
    </head>
    <body>
        <input type="text" id="myInput" onkeyup="myFunction()" placeholder="Search for names.." title="Type in a name">
        <ul id="myUL">
        <li><a href="#">#1:</a></li>
        <li><a href="#">#2:</a></li>
        <li><a href="#">#3:</a></li>
        <li><a href="#">#4:</a></li>
        <li><a href="#">#5:</a></li>
        <li><a href="#">#6:</a></li>
        <li><a href="#">#7:</a></li>
        </ul>
                <a style="color: white; font-size: 25px;" href="https://mcallisterschool.github.io/places/">home</a>        
        <script>
            function myFunction() {
                var input, filter, ul, li, a, i, txtValue;
                input = document.getElementById("myInput");
                filter = input.value.toUpperCase();
                ul = document.getElementById("myUL");
                li = ul.getElementsByTagName("li");
                for (i = 0; i < li.length; i++) {
                    a = li[i].getElementsByTagName("a")[0];
                    txtValue = a.textContent || a.innerText;
                    if (txtValue.toUpperCase().indexOf(filter) > -1) {
                        li[i].style.display = "";
                    } else {
                        li[i].style.display = "none";
                    }
                }
            }
            </script>
    </body>
</html>
