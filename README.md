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
