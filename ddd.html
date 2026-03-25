<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bảng Xếp Hạng - Chỉnh Sửa & Lưu Trữ</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .top-1 { border-left: 5px solid #fbbf24; }
        .top-2 { border-left: 5px solid #9ca3af; }
        .top-3 { border-left: 5px solid #fb923c; }
    </style>
</head>
<body class="bg-slate-50 min-h-screen p-4 md:p-10">

    <div class="max-w-5xl mx-auto bg-white shadow-2xl rounded-2xl overflow-hidden">
        <div class="bg-gradient-to-r from-blue-700 to-indigo-800 p-8 text-white">
            <h1 class="text-3xl font-black uppercase tracking-tighter">Leaderboard Pro</h1>
            <p class="text-blue-100 opacity-80">Nhập liệu - Tự động xếp hạng - Lưu trữ vĩnh viễn</p>
        </div>

        <div class="p-6 md:p-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-4 mb-10 bg-slate-100 p-6 rounded-xl border border-slate-200">
                <input type="text" id="inputName" placeholder="Họ tên" class="p-3 rounded-lg border focus:ring-2 focus:ring-blue-500 outline-none">
                <input type="text" id="inputMSV" placeholder="Mã SV" class="p-3 rounded-lg border focus:ring-2 focus:ring-blue-500 outline-none font-mono">
                <input type="number" id="inputScore" placeholder="Điểm (0-10)" step="0.1" class="p-3 rounded-lg border focus:ring-2 focus:ring-blue-500 outline-none">
                <button onclick="addStudent()" class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 rounded-lg transition-all shadow-lg active:scale-95">
                    Thêm & Xếp Hạng
                </button>
            </div>

            <div class="overflow-x-auto rounded-xl border border-slate-200">
                <table class="w-full text-left border-collapse">
                    <thead class="bg-slate-800 text-white">
                        <tr>
                            <th class="p-4 text-center w-20">Hạng</th>
                            <th class="p-4">Sinh Viên</th>
                            <th class="p-4">Mã Số</th>
                            <th class="p-4 text-center cursor-pointer hover:bg-slate-700" onclick="toggleSort()">
                                Điểm <span id="sortIcon">▼</span>
                            </th>
                            <th class="p-4 text-center w-32">Thao Tác</th>
                        </tr>
                    </thead>
                    <tbody id="leaderboardBody" class="divide-y divide-slate-200">
                        </tbody>
                </table>
            </div>
            
            <div class="mt-6 flex justify-end">
                <button onclick="clearAll()" class="text-red-500 hover:text-red-700 text-sm font-semibold underline">
                    Xóa tất cả danh sách
                </button>
            </div>
        </div>
    </div>

    <script>
        // Khởi tạo dữ liệu từ LocalStorage (nếu có) hoặc mảng rỗng
        let students = JSON.parse(localStorage.getItem('studentData')) || [];
        let sortAsc = false;

        function updateStorage() {
            localStorage.setItem('studentData', JSON.stringify(students));
        }

        function addStudent() {
            const name = document.getElementById('inputName').value.trim();
            const msv = document.getElementById('inputMSV').value.trim();
            const score = parseFloat(document.getElementById('inputScore').value);

            if (!name || !msv || isNaN(score)) return alert("Vui lòng nhập đủ thông tin!");

            students.push({ id: Date.now(), name, msv, score });
            render();
            
            // Clear input
            document.getElementById('inputName').value = '';
            document.getElementById('inputMSV').value = '';
            document.getElementById('inputScore').value = '';
        }

        function deleteStudent(id) {
            if(confirm("Xóa sinh viên này?")) {
                students = students.filter(s => s.id !== id);
                render();
            }
        }

        function editStudent(id) {
            const student = students.find(s => s.id === id);
            const newName = prompt("Sửa tên:", student.name);
            const newScore = prompt("Sửa điểm:", student.score);
            
            if (newName !== null) student.name = newName;
            if (newScore !== null && !isNaN(parseFloat(newScore))) student.score = parseFloat(newScore);
            
            render();
        }

        function toggleSort() {
            sortAsc = !sortAsc;
            document.getElementById('sortIcon').textContent = sortAsc ? "▲" : "▼";
            render();
        }

        function clearAll() {
            if(confirm("Bạn có chắc chắn muốn xóa sạch danh sách?")) {
                students = [];
                render();
            }
        }

        function render() {
            // Sắp xếp
            students.sort((a, b) => sortAsc ? a.score - b.score : b.score - a.score);
            updateStorage();

            const body = document.getElementById('leaderboardBody');
            body.innerHTML = '';

            students.forEach((s, i) => {
                const isTop = i < 3 && !sortAsc;
                const topClass = isTop ? `top-${i+1} bg-orange-50/50` : '';
                
                body.innerHTML += `
                    <tr class="${topClass} hover:bg-slate-50 transition-all">
                        <td class="p-4 text-center font-black text-lg ${isTop ? 'text-orange-600' : 'text-slate-400'}">
                            ${i + 1}
                        </td>
                        <td class="p-4 font-semibold text-slate-700">${s.name}</td>
                        <td class="p-4 font-mono text-sm text-slate-500">${s.msv}</td>
                        <td class="p-4 text-center font-bold text-blue-700">${s.score}</td>
                        <td class="p-4 text-center space-x-2">
                            <button onclick="editStudent(${s.id})" class="text-blue-500 hover:text-blue-700 p-1">Sửa</button>
                            <button onclick="deleteStudent(${s.id})" class="text-red-500 hover:text-red-700 p-1">Xóa</button>
                        </td>
                    </tr>
                `;
            });
        }

        // Chạy lần đầu
        render();
    </script>
</body>
</html>
