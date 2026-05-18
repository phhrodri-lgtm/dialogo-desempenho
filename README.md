<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ReportFlow - Sistema de Relatórios</title>
    
    <!-- Scripts e Fontes -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" rel="stylesheet">
    
    <style>
        body { 
            background-color: #f7f9fb; 
            font-family: 'Inter', sans-serif; 
        }
        .glass-card { 
            background: white; 
            border: 1px solid #e2e8f0; 
            border-radius: 1rem; 
            padding: 1.5rem; 
            margin-bottom: 1rem; 
            box-shadow: 0 1px 3px rgba(0,0,0,0.1); 
        }
        .material-symbols-outlined {
            vertical-align: middle;
        }
    </style>
</head>
<body class="pb-20">

    <!-- Cabeçalho (Onde aparece analytics e ReportFlow) -->
    <header class="bg-white border-b p-4 sticky top-0 z-50">
        <div class="max-w-5xl mx-auto flex justify-between items-center">
            <div class="flex items-center gap-2 text-teal-600">
                <span class="material-symbols-outlined text-3xl">analytics</span>
                <span class="font-bold text-xl text-black">ReportFlow</span>
            </div>
            <div class="w-10 h-10 bg-gray-200 rounded-full flex items-center justify-center">
                <span class="material-symbols-outlined text-gray-600">person</span>
            </div>
        </div>
    </header>

    <main class="max-w-5xl mx-auto p-6">
        <div class="mb-8">
            <h2 class="text-2xl font-bold">Histórico de Relatórios</h2>
            <p class="text-gray-500">Gerencie seus dados e visualizações.</p>
        </div>

        <!-- Lista de Relatórios (Exemplos) -->
        <div id="lista">
            <div class="glass-card flex justify-between items-center border-l-4 border-l-teal-500">
                <div>
                    <h4 class="font-bold text-gray-800">Desempenho Geral</h4>
                    <p class="text-sm text-gray-500">Atualizado hoje às 14:00</p>
                </div>
                <span class="material-symbols-outlined text-teal-600">chevron_right</span>
            </div>

            <div class="glass-card flex justify-between items-center border-l-4 border-l-gray-300">
                <div>
                    <h4 class="font-bold text-gray-800">Controle de Estoque</h4>
                    <p class="text-sm text-gray-500">Aguardando sincronização</p>
                </div>
                <span class="material-symbols-outlined text-gray-400">lock</span>
            </div>
        </div>
    </main>

    <!-- Navegação Inferior (Mobile) -->
    <nav class="fixed bottom-0 w-full bg-white border-t flex justify-around p-4 md:hidden">
        <span class="material-symbols-outlined text-teal-600">home</span>
        <span class="material-symbols-outlined text-gray-400">search</span>
        <span class="material-symbols-outlined text-gray-400">settings</span>
    </nav>

</body>
</html>
