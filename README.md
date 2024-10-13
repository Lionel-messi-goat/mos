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

