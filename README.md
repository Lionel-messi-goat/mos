<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>전화번호 저장</title>
</head>
<body>
    <h1>전화번호 저장</h1>
    <form action="/save" method="get">
        이름: <input type="text" name="name" required><br>
        전화번호: <input type="text" name="phone" required><br>
        <button type="submit">저장</button>
    </form>

    <h1>전화번호 검색</h1>
    <form action="/search" method="post">
        이름: <input type="text" name="name" required><br>
        <button type="submit">검색</button>
    </form>

    <a href="/all">전체 전화번호 보기</a>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>전화번호 검색 결과</title>
</head>
<body>
    <h1>검색 결과</h1>
    {% if phone %}
        <p>{{ name }}: {{ phone }}</p>
    {% else %}
        <p>{{ name }}에 대한 전화번호를 찾을 수 없습니다.</p>
    {% endif %}
    
    <a href="/">전화번호 저장/검색으로 돌아가기</a>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>전체 전화번호부</title>
</head>
<body>
    <h1>전체 전화번호 목록</h1>
    <ul>
        {% for name, phone in phonebook %}
            <li>{{ name }}: {{ phone }}</li>
        {% endfor %}
    </ul>
    
    <a href="/">전화번호 저장/검색으로 돌아가기</a>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>전화번호부</title>
</head>
<body>
    <h1>전화번호 저장</h1>
    <form action="/store/" method="get">
        이름: <input type="text" name="name" required><br>
        전화번호: <input type="text" name="tel" required><br>
        <button type="submit">저장</button>
    </form>
    {% if msg %}
        <p>{{ msg }}</p>
    {% endif %}

    <h1>전화번호 검색</h1>
    <form action="/search/" method="post">
        이름: <input type="text" name="name" required><br>
        <button type="submit">검색</button>
    </form>
    {% if search_result %}
        <p>{{ search_name }}의 전화번호: {{ search_result }}</p>
    {% elif search_name %}
        <p>{{ search_name }}에 대한 결과가 없습니다.</p>
    {% endif %}
    
    <a href="/all/">전체 전화번호 보기</a>
</body>
</html>


input[type=text]:hover {
        border : 2px solid skyblue
}

table { /* 이중 테두리 제거 */
        border-collapse : collapse;
}
td, th { /* 모든 셀에 적용 */
        text-align : left;
        padding : 5px;
        height : 15px;
        width : 100px;
        border-bottom : 1px solid gray;
}
thead, tfoot { /* <thead>의 모든 셀에 적용 */
        background : darkgray;
        color : yellow;
}
tbody tr:nth-child(even) { /* 짝수 <tr>에 적용*/
        background : aliceblue;
}
tbody tr:hover { /* 마우스가 올라오면 pink 배경 */
        background : pink;
}
![image](https://github.com/user-attachments/assets/21dcbec4-5793-422c-9063-7fb4bd8f836a)

