<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="utf-8">
    <meta content="width=device-width, initial-scale=1.0" name="viewport">
    <title>ReportFlow - Sistema de Relatórios</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" rel="stylesheet">
    <style>
        body { background-color: #f7f9fb; font-family: 'Inter', sans-serif; }
        .glass-card { background: white; border: 1px solid #e2e8f0; border-radius: 1rem; padding: 1.5rem; shadow: 0 1px 3px rgba(0,0,0,0.1); }
    </style>
</head>
<body class="pb-20">
    <header class="bg-white border-b p-4 sticky top-0 z-50">
        <div class="max-w-5xl mx-auto flex justify-between items-center">
            <div class="flex items-center gap-2 text-teal-600">
                <span class="material-symbols-outlined">analytics</span>
                <span class="font-bold text-xl text-black">ReportFlow</span>
            </div>
            <div class="w-10 h-10 bg-gray-200 rounded-full"></div>
        </div>
    </header>

    <main class="max-w-5xl mx-auto p-6">
        <div class="mb-8">
            <h2 class="text-2xl font-bold">Histórico de Relatórios</h2>
            <p class="text-gray-500">Visualize seus relatórios emitidos</p>
        </div>

        <div class="relative mb-6">
            <span class="material-symbols-outlined absolute left-3 top-3 text-gray-400">search</span>
            <input type="text" id="busca" class="w-full pl-10 pr-4 py-2 border rounded-xl outline-none focus:ring-2 focus:ring-teal-500" placeholder="Buscar relatório...">
        </div>

        <div class="grid gap-4" id="lista">
            <!-- Relatório 1 -->
            <div class="glass-card flex justify-between items-center border-l-4 border-l-green-500">
                <div>
                    <h4 class="font-bold text-gray-800">Performance Industrial</h4>
                    <p class="text-sm text-gray-500">14/06/2024 • Enviado</p>
                </div>
                <button class="text-teal-600 font-bold hover:underline">Ver</button>
            </div>
            <!-- Relatório 2 -->
            <div class="glass-card flex justify-between items-center border-l-4 border-l-amber-500">
                <div>
                    <h4 class="font-bold text-gray-800">Auditoria de Segurança</h4>
                    <p class="text-sm text-gray-500">12/06/2024 • Pendente</p>
                </div>
                <button class="text-teal-600 font-bold hover:underline">Completar</button>
            </div>
        </div>
    </main>

    <nav class="fixed bottom-0 w-full bg-white border-t flex justify-around p-4 md:hidden">
        <span class="material-symbols-outlined text-gray-400">dashboard</span>
        <span class="material-symbols-outlined text-teal-600">assessment</span>
        <span class="material-symbols-outlined text-gray-400">person</span>
    </nav>

    <script>
        document.getElementById('busca').addEventListener('input', function(e) {
            const termo = e.target.value.toLowerCase();
            const cards = document.querySelectorAll('#lista > div');
            cards.forEach(card => {
                const texto = card.innerText.toLowerCase();
                card.style.display = texto.includes(termo) ? 'flex' : 'none';
            });
        });
    </script>
</body>
</html>
