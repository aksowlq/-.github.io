<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Scentory</title>
  <style>
    /* 기본 스타일 */
    body {
      font-family: 'Arial', sans-serif; 
      margin: 0; 
      padding: 0; 
      box-sizing: border-box; 
      background-color: #faf0e5;
    }

    header {
      background-color: #fccaca; 
      color: #fff; 
      text-align: center; 
      padding: 10px 0;
      border-bottom: 1px solid #e5e5e5;
      
    }

    .top-bar {
      max-width: 1200px;
      margin: 0 auto;
      padding: 15px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    
    .logo {
     font-size: 28px;
    font-weight: bold;
    color: #fff;
    letter-spacing: 1px;
    text-decoration: none; 
    }
    /* 네비게이션 */
    nav {
      flex-grow: 1;
      text-align: center;
    }

    nav a {
      margin: 0 15px;
      text-decoration: none;
      color: #fff;
      font-size: 18px;
    }

    nav a:hover {
      font-weight: bold;
    }

    .icons {
      display: flex;
      align-items: center;
    }

    .icons span {
      margin-left: 15px;
      font-size: 20px;
      cursor: pointer;
    }

    /* 본문 스타일 */
    main {
      max-width: 1200px;
      margin: 0 auto;
      padding: 20px;
    }

    .filters {
      width: 200px;
      float: left;
      margin-right: 20px;
    }
    .filters span {
    display: inline-block;
    margin-right: -12px; /* 오른쪽으로 10px 여백 추가 */
    }
    .filters h3 {
      margin-bottom: 10px;
      font-size: 16px;
      font-weight: bold;
      color: #5b5b5b;
    }

    .filters label {
      display: block;
      margin-top: 10px;
      font-size: 14px;
      color: #333;
    }

    .filters input,
    .filters select {
      width: 100%;
      margin-top: 5px;
      padding: 5px;
      font-size: 14px;
    }
    input[type="range"] {
  accent-color: #5b5b5b; /* 슬라이더 진행 상태 색상 */
}
    .product-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .product {
      border: 1px solid #e5e5e5;
      border-radius: 5px;
      text-align: center;
      padding: 10px;
      background-color: #fff;
    }

    .product img {
      max-width: 100%;
      height: auto;
      border-bottom: 1px solid #e5e5e5;
      margin-bottom: 10px;
      padding-bottom: 10px;
    }

    .product p {
      margin: 5px 0;
      font-size: 14px;
      color: #333;
    }

    .product-name {
      font-size: 16px;
      font-weight: bold;
      margin: 10px 0;
    }

    .product button {
      padding: 5px 10px;
      background-color: #fccaca;
      color: #fff;
      border: none;
      border-radius: 3px;
      cursor: pointer;
      font-size: 14px;
    }

    .product button:hover {
      background-color: #d39b9b;
    }
    footer {
  background-color: #fccaca;
  color: #fff;
  text-align: center;
  padding: 10px 0;
  position: relative; /* 고정 위치 제거 */
  width: 100%; /* 화면 전체 너비를 차지 */
}
    /* 반응형 디자인 */
    @media screen and (max-width: 768px) {
      .product-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    @media screen and (max-width: 480px) {
      .product-grid {
        grid-template-columns: 1fr;
      }
    }
    #search-container {
  background-color: #fff;
  width: 170px;
  height: 30px;
  margin-top: 5px;
  padding-left: 10px;
  border-radius: 5px;
  border: 1px solid #e5e5e5;
  position: absolute;  /* absolute 위치로 설정 */
  top: 40px;  /* 상단에 위치 조정 */
  right: 80px;  /* 오른쪽에 위치하도록 설정 (장바구니 아이콘과 간격을 맞춤) */
  display: flex;
  align-items: center;
}
    #search-container .search-container-icons img {
  width: 30px;  /* 이미지 크기 변경 */
  height: auto;  /* 비율에 맞게 높이 자동 조정 */
}

#search-container input {
  width: 100%;
  height: 100%;
  border: none;
  outline: none;
  font-size: 12px;
  padding: 0; /* 불필요한 여백 제거 */
  color: #333; /* 텍스트 색상 */
  padding-right: 30px;
}
#search-container .search-icon {
  position: absolute;
  top: 50%;
  right: 0px;  /* 오른쪽 끝에 위치 */
  transform: translateY(-50%);  /* 세로 중앙 정렬 */
  width: 20px;  /* 이미지 크기 설정 */
  height: 20px;
  cursor: pointer;
}
#search-container input::placeholder {
  color: #999; /* "검색어를 입력하세요" 텍스트 색상 */
}


  </style>
</head>
<body>
  <!-- 헤더 -->
  <header>
    <div class="top-bar">
      <!-- 로고 -->
      <a href="file:///C:/Users/k9952/OneDrive/바탕 화면/첫화면.html" class="logo">Scentory</a>
      
      <!-- 네비게이션 -->
      <nav>
        <a href="file:///C:/Users/k9952/OneDrive/%EB%B0%94%ED%83%95%20%ED%99%94%EB%A9%B4/%EC%A0%84%EC%B2%B4%EC%83%81%ED%92%88.html">전체상품</a>
        <a href="#">스킨케어</a>
        <a href="#">메이크업</a>
        <a href="#">헤어케어</a>
        <a href="#">퍼퓸</a>
        <a href="#">기타</a>
      </nav>
  
      <!-- 아이콘 -->
      <div class="icons">
        <img src="images/wkdqkrnsl.jpg" alt="장바구니 이미지" style="width: 24px; height: 24px;">
      </div>
    </div>
  </header>
  <div id="search-container">
    <input type="text" placeholder="검색어를 입력해주세요.">
    <div class="search-container-icons">
      <img src="images/eheqhrl.jpg" alt="장바구니 이미지" class="search-icon">
    </div>
  </div>
  <!-- 본문 -->
  <main>
    <!-- 왼쪽 필터 -->
    <div class="filters">
      <h3>검색 옵션</h3>
      <div>
        <label for="price">가격</label>
        <div style="display: flex; justify-content: space-between; font-size: 12px;">
          <span>₩0</span>
          <span>₩100,000</span>
        </div>
        <input type="range" id="price" min="0" max="100000" value="50000" step="1000" style="width: 100%; height: 8px; background-color: #fccaca; border-radius: 5px;">
      </div>
      <div>
        <label for="category">전체 상품</label>
        <select id="category">
          <option>스킨</option>
          <option>로션</option>
          <option>수분</option>
          <option>헤어케어</option>
          <option>바디케어</option>
          <option>기타</option>
        </select>
      </div>
    </div>
    
    <!-- 제품 목록 -->
    <section class="product-grid" id="product-grid">
      <h2 style="grid-column: span 3; text-align: left; color: #5b5b5b; ">전체 상품</h2>
      <!-- 제품 카드 -->
      <div class="product" data-price="15000">
        <a href="file:///C:/Users/k9952/OneDrive/%EB%B0%94%ED%83%95%20%ED%99%94%EB%A9%B4/%EC%83%81%EC%84%B8%ED%8E%98%EC%9D%B4%EC%A7%80.html" style="text-decoration: none; color: inherit;">
          <img src="images/product1.jpg" alt="Product 1">
          <p class="product-name">Product 1 Name</p>
          <p class="product-price">₩15,000</p>
          <button>ADD TO CART</button>
        </a>
      </div>
      <div class="product" data-price="20000">
        <img src="images/product2.jpg" alt="Product 2">
        <p class="product-name">Product 2 Name</p>
        <p class="product-price">₩20,000</p>
        <button>ADD TO CART</button>
      </div>
      <div class="product" data-price="25000">
        <img src="images/product3.jpg" alt="Product 3">
        <p class="product-name">Product 3 Name</p>
        <p class="product-price">₩25,000</p>
        <button>ADD TO CART</button>
      </div>
      <div class="product" data-price="30000">
        <img src="images/product4.jpg" alt="Product 4">
        <p class="product-name">Product 4 Name</p>
        <p class="product-price">₩30,000</p>
        <button>ADD TO CART</button>
      </div>
      <div class="product" data-price="35000">
        <img src="images/product5.jpg" alt="Product 5">
        <p class="product-name">Product 5 Name</p>
        <p class="product-price">₩35,000</p>
        <button>ADD TO CART</button>
      </div>
      <div class="product" data-price="40000">
        <img src="images/product6.jpg" alt="Product 6">
        <p class="product-name">Product 6 Name</p>
        <p class="product-price">₩40,000</p>
        <button>ADD TO CART</button>
      </div>
    </section>
  </main>
  
  <!-- 푸터 -->
  <footer>
    <p>&copy; 2024 Scentory. All rights reserved.</p>
  </footer>

  <script>
    const priceSlider = document.getElementById('price');
    const productGrid = document.getElementById('product-grid');
  
    // 가격 필터링 함수
    function filterProducts() {
      const maxPrice = priceSlider.value;
      const products = document.querySelectorAll('.product');
  
      products.forEach(product => {
        const productPrice = parseInt(product.getAttribute('data-price'));
        if (productPrice <= maxPrice) {
          product.style.display = 'block';
        } else {
          product.style.display = 'none';
        }
      });
    }
  
    priceSlider.addEventListener('input', filterProducts);
  
    // 처음 페이지 로드 시 필터링
    filterProducts();

    const eheqhrlImage = document.querySelector('img[alt="장바구니 이미지"]'); // eheqhrl 이미지
const searchContainer = document.getElementById('search-container');

eheqhrlImage.addEventListener('click', function() {
  // 검색창을 보이게 하거나 숨기기
  if (searchContainer.style.display === 'none' || searchContainer.style.display === '') {
    searchContainer.style.display = 'block';
  } else {
    searchContainer.style.display = 'none';
  }
});
  </script>
</body>
</html>
