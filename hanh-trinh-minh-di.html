<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hành Trình Mình Đi</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 20px;
        }
        #grid {
            display: grid;
            grid-template-columns: repeat(10, 1fr);
            gap: 10px;
            margin-top: 20px;
            justify-content: center;
        }
        .province {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }
        .circle {
            width: 80px;
            height: 80px;
            border-radius: 80%;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            cursor: pointer;
            overflow: hidden;
            position: relative;
        }
        .circle img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
        }
        input[type="file"] {
            display: none;
        }
        input[type="text"] {
            width: 100px;
            text-align: center;
            font-size: 14px;
            border: none;
            background: none;
            outline: none;
        }
    </style>
</head>
<body>

    <h1>Hành Trình Mình Đi</h1>

    <div id="grid"></div>

    <script>
        // Danh sách 63 tỉnh thành
        let defaultProvinces = [
            "An Giang", "Bà Rịa - Vũng Tàu", "Bắc Giang", "Bắc Kạn", "Bạc Liêu", "Bắc Ninh", "Bến Tre", "Bình Định", "Bình Dương", "Bình Phước",
            "Bình Thuận", "Cà Mau", "Cần Thơ", "Cao Bằng", "Đà Nẵng", "Đắk Lắk", "Đắk Nông", "Điện Biên", "Đồng Nai", "Đồng Tháp",
            "Gia Lai", "Hà Giang", "Hà Nam", "Hà Nội", "Hà Tĩnh", "Hải Dương", "Hải Phòng", "Hậu Giang", "Hòa Bình", "Hưng Yên",
            "Khánh Hòa", "Kiên Giang", "Kon Tum", "Lai Châu", "Lâm Đồng", "Lạng Sơn", "Lào Cai", "Long An", "Nam Định", "Nghệ An",
            "Ninh Bình", "Ninh Thuận", "Phú Thọ", "Phú Yên", "Quảng Bình", "Quảng Nam", "Quảng Ngãi", "Quảng Ninh", "Quảng Trị", "Sóc Trăng",
            "Sơn La", "Tây Ninh", "Thái Bình", "Thái Nguyên", "Thanh Hóa", "Thừa Thiên Huế", "Tiền Giang", "TP Hồ Chí Minh", "Trà Vinh", "Tuyên Quang",
            "Vĩnh Long", "Vĩnh Phúc", "Yên Bái"
        ];

        // Lấy danh sách tỉnh từ Local Storage (nếu có), nếu không thì dùng danh sách mặc định
        let provinces = JSON.parse(localStorage.getItem("provinces")) || [...defaultProvinces];

        const grid = document.getElementById("grid");

        function renderProvinces() {
            grid.innerHTML = ""; // Xóa lưới cũ trước khi render mới

            provinces.forEach(province => {
                createProvinceElement(province);
            });

            // Nút thêm địa điểm
            let addBtn = document.createElement("div");
            addBtn.className = "province";
            addBtn.innerHTML = `
                <div class="circle" style="font-size: 32px;">+</div>
                <p>Thêm địa điểm</p>
            `;
            addBtn.onclick = addProvince;
            grid.appendChild(addBtn);
        }

        function createProvinceElement(province) {
            let container = document.createElement("div");
            container.className = "province";

            let circle = document.createElement("div");
            circle.className = "circle";
            circle.textContent = "+";
            circle.onclick = () => fileInput.click();

            let savedImage = localStorage.getItem(province);
            if (savedImage) {
                setImage(circle, savedImage, province);
            }

            let label = document.createElement("p");
            label.textContent = province;
            label.style.cursor = "pointer";
            label.onclick = () => editProvinceName(label);

            let fileInput = document.createElement("input");
            fileInput.type = "file";
            fileInput.accept = "image/*";
            fileInput.onchange = event => handleImageUpload(event, circle, province);

            container.appendChild(circle);
            container.appendChild(fileInput);
            container.appendChild(label);
            grid.appendChild(container);
        }

        function handleImageUpload(event, circle, province) {
            let file = event.target.files[0];
            if (file) {
                let reader = new FileReader();
                reader.onload = e => {
                    setImage(circle, e.target.result, province);
                    localStorage.setItem(province, e.target.result);
                };
                reader.readAsDataURL(file);
            }
        }

        function setImage(circle, src, province) {
            let img = document.createElement("img");
            img.src = src;
            img.oncontextmenu = function (e) {
                e.preventDefault();
                if (confirm("Bạn có muốn xóa ảnh này không?")) {
                    localStorage.removeItem(province);
                    circle.innerHTML = "+";
                }
            };
            circle.innerHTML = "";
            circle.appendChild(img);
        }

        function editProvinceName(label) {
            let input = document.createElement("input");
            input.type = "text";
            input.value = label.textContent;
            input.onblur = () => {
                label.textContent = input.value;
                label.style.display = "block";
                input.remove();
            };
            input.onkeypress = event => {
                if (event.key === "Enter") {
                    input.blur();
                }
            };

            label.style.display = "none";
            label.parentNode.appendChild(input);
            input.focus();
        }

        function addProvince() {
            let newProvince = prompt("Nhập tên địa điểm mới:");
            if (newProvince && !provinces.includes(newProvince)) {
                provinces.push(newProvince);
                localStorage.setItem("provinces", JSON.stringify(provinces));
                renderProvinces();
            }
        }

        renderProvinces();
    </script>

</body>
</html>
