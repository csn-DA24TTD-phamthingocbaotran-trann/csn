
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website quản lý học viên - Trung tâm ngoại ngữ</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #f1f5f9;
            color: #1e293b;
        }

        button, input, select {
            font: inherit;
        }

        button {
            padding: 10px 14px;
            background: #2563eb;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            opacity: 0.88;
        }

        input, select {
            width: 100%;
            padding: 10px;
            margin: 6px 0;
            border: 1px solid #cbd5e1;
            border-radius: 5px;
            background: white;
        }

        .login-box {
            width: 360px;
            max-width: 92%;
            margin: 90px auto;
            padding: 25px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 15px #cbd5e1;
        }

        .login-box h2 {
            text-align: center;
            color: #2563eb;
        }

        .login-message {
            color: #dc2626;
            text-align: center;
        }

        .container {
            display: none;
        }

        header {
            background: #1e40af;
            color: white;
            padding: 18px 24px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 12px;
        }

        header h2 {
            margin: 0 0 8px;
            color: white;
        }

        .logout-button {
            background: #dc2626;
        }

        nav {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            padding: 12px 20px;
            background: #dbeafe;
        }

        nav button {
            background: transparent;
            color: #1e40af;
            font-weight: bold;
        }

        nav button.active,
        nav button:hover {
            background: #2563eb;
            color: white;
        }

        main {
            padding: 22px;
            max-width: 1400px;
            margin: auto;
        }

        .page {
            display: none;
        }

        .page.active {
            display: block;
        }

        .card {
            background: white;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 7px #e2e8f0;
        }

        .card h2 {
            margin-top: 0;
            color: #1d4ed8;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 16px;
        }

        .stat-card {
            padding: 20px;
            background: white;
            border-left: 5px solid #2563eb;
            border-radius: 8px;
            box-shadow: 0 2px 7px #e2e8f0;
        }

        .stat-card p {
            margin-bottom: 5px;
            color: #64748b;
        }

        .stat-card strong {
            font-size: 28px;
            color: #1d4ed8;
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            gap: 10px 16px;
        }

        .form-group label {
            display: block;
            font-weight: bold;
            font-size: 14px;
            margin-top: 5px;
        }

        .form-actions {
            display: flex;
            gap: 10px;
            margin-top: 12px;
        }

        .secondary {
            background: #64748b;
        }

        .success {
            background: #16a34a;
        }

        .danger {
            background: #dc2626;
        }

        .search-box {
            max-width: 450px;
            margin-bottom: 15px;
        }

        .table-wrap {
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            min-width: 650px;
        }

        th, td {
            padding: 11px;
            border: 1px solid #cbd5e1;
            text-align: left;
        }

        th {
            background: #dbeafe;
            color: #1e40af;
        }

        tbody tr:nth-child(even) {
            background: #f8fafc;
        }

        .table-button {
            padding: 7px 10px;
            margin: 2px;
        }

        .empty {
            text-align: center;
            color: #64748b;
            padding: 20px;
        }

        .status-present {
            color: #15803d;
            font-weight: bold;
        }

        .status-absent {
            color: #dc2626;
            font-weight: bold;
        }

        footer {
            text-align: center;
            padding: 18px;
            background: #e2e8f0;
            color: #475569;
        }

        @media (max-width: 700px) {
            header {
                align-items: flex-start;
                flex-direction: column;
            }

            main {
                padding: 12px;
            }

            .form-grid, .stats {
                grid-template-columns: 1fr;
            }

            .card {
                padding: 14px;
            }
        }
    </style>
</head>

<body>
