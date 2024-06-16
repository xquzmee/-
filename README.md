<!DOCTYPE html>
<html>
<head>
    <title>Каталог програмної системи з калькулятором нелінійних рівнянь</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(300deg, #d8bfd8, #a020f0, #d8bfd8);
            background-size: 180% 180%;
            animation: gradient-animation 18s ease infinite;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        @keyframes gradient-animation {
            0% {
                background-position: 0% 50%;
            }

            50% {
                background-position: 100% 50%;
            }

            100% {
                background-position: 0% 50%;
            }
        }

        h1 {
            text-align: center;
            color: #fff;
            margin-bottom: 20px;
        }

        nav {
            background-color: rgba(255, 255, 255, 0.8);
            padding: 10px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
        }

            nav ul {
                list-style-type: none;
                margin: 0;
                padding: 0;
                display: flex;
            }

            nav li {
                margin-right: 10px;
            }

            nav a, nav button {
                text-decoration: none;
                color: #333;
                padding: 5px 10px;
                border-radius: 5px;
                cursor: pointer;
                border: none;
                background-color: transparent;
            }

                nav a:hover, nav button:hover {
                    background-color: #a020f0;
                    color: #fff;
                }

        .content {
            background-color: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

            .content ul {
                list-style-type: none;
                padding: 0;
            }

            .content li {
                margin-bottom: 5px;
            }

        form {
            margin-bottom: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        label {
            display: block;
            margin-bottom: 5px;
            color: #333;
        }

        input[type="text"] {
            padding: 5px;
            width: 300px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            padding: 5px 10px;
            background-color: #a020f0;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 10px;
        }

        #result {
            margin-top: 20px;
            font-weight: bold;
            background-color: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        #chart-container {
            width: 100%;
            max-width: 600px;
            background-color: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        #history-container {
            background-color: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
        }

            #history-container h3 {
                margin-top: 0;
            }
    </style>
</head>
<body>
    <h1>Каталог програмної системи</h1>
    <nav>
        <ul>
            <li><a href="#" id="catalog-btn">Каталог</a></li>
            <li><a href="#" id="equation-btn">Калькулятор рівнянь</a></li>
            <li><a href="#" id="delivery-btn">Спосіб доставки</a></li>
            <li><a href="#" id="payment-btn">Спосіб оплати</a></li>
        </ul>
    </nav>

    <div id="catalog-content" class="content" style="display: none;">
        <h2>Каталог</h2>
        <ul>
            <li><button id="antiviruses-btn">Антивіруси</button></li>
            <li><button id="os-btn">Операційні системи</button></li>
            <li><button id="office-btn">Офісні програми</button></li>
            <li><button id="utilities-btn">Утиліти</button></li>
        </ul>
    </div>

    <div id="antiviruses-content" class="content" style="display: none;">
        <h2>Антивіруси</h2>
        <ul>
            <li>Антивірус 1</li>
            <li>Антивірус 2</li>
            <li>Антивірус 3</li>
        </ul>
    </div>

    <div id="os-content" class="content" style="display: none;">
        <h2>Операційні системи</h2>
        <ul>
            <li>Операційна система 1</li>
            <li>Операційна система 2</li>
            <li>Операційна система 3</li>
        </ul>
    </div>

    <div id="office-content" class="content" style="display: none;">
        <h2>Офісні програми</h2>
        <ul>
            <li>Офісна програма 1</li>
            <li>Офісна програма 2</li>
            <li>Офісна програма 3</li>
        </ul>
    </div>

    <div id="utilities-content" class="content" style="display: none;">
        <h2>Утиліти</h2>
        <ul>
            <li>Утиліта 1</li>
            <li>Утиліта 2</li>
            <li>Утиліта 3</li>
        </ul>
    </div>

    <div id="delivery-content" class="content" style="display: none;">
        <h2>Спосіб доставки</h2>
        <p>Тут буде вибір способу доставки.</p>
    </div>

    <div id="payment-content" class="content" style="display: none;">
        <h2>Спосіб оплати</h2>
        <ul>
            <li>Тут буду вибір способу оплати.</li>
        </ul>
    </div>

    <div id="equation-content" class="content" style="display: none;">
        <h2>Нелінійні рівняння</h2>
        <form>
            <label for="equation">Рівняння:</label>
            <input type="text" id="equation" placeholder="Введіть рівняння" value="x**3 - 2*x + 1">
            <label for="initial-guess">Початкове наближення:</label>
            <input type="text" id="initial-guess" placeholder="Введіть початкове наближення" value="1.0">
            <button type="button" onclick="solveEquation()">Розв'язати</button>
            <button type="button" onclick="showGraph()">Графік</button>
        </form>
        <div id="result"></div>
        <div id="chart-container">
            <canvas id="chart"></canvas>
        </div>
        <div id="history-container">
            <h3>Історія вирішення</h3>
            <ul id="history-list"></ul>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script>
        let chart;
        const historyList = document.getElementById('history-list');

        function solveEquation() {
            const equationInput = document.getElementById("equation").value;
            const initialGuessInput = document.getElementById("initial-guess").value;

            // Створення екземплярів вирішувачів
            const newtonSolver = new NewtonRaphsonSolver();
            const secantSolver = new SecantSolver();
            const bisectionSolver = new BisectionSolver();

            // Функція для обчислення рівняння
            const equation = new Function("x", `return ${equationInput}`);

            // Знаходження коренів рівняння
            const rootNewton = newtonSolver.solve(equation, parseFloat(initialGuessInput));
            const rootSecant = secantSolver.solve(equation, parseFloat(initialGuessInput));
            const rootBisection = bisectionSolver.solve(equation, 0.0, 2.0);

            // Виведення результатів
            const resultDiv = document.getElementById("result");
            resultDiv.innerHTML = `
                                <p>Корінь рівняння (метод Ньютона-Рафсона): ${rootNewton}</p>
                                <p>Корінь рівняння (метод січних): ${rootSecant}</p>
                                <p>Корінь рівняння (метод бісекції): ${rootBisection}</p>
                            `;

            // Додавання запису до історії
            const historyItem = document.createElement('li');
            historyItem.textContent = `Рівняння: ${equationInput}, Початкове наближення: ${initialGuessInput}, Корені: ${rootNewton}, ${rootSecant}, ${rootBisection}`;
            historyList.appendChild(historyItem);
        }

        function showGraph() {
            const equationInput = document.getElementById("equation").value;
            const equation = new Function("x", `return ${equationInput}`);

            const data = {
                labels: [],
                datasets: [{
                    label: 'Рівняння',
                    data: [],
                    borderColor: 'rgba(160, 32, 240, 1)',
                    fill: false
                }]
            };

            const xValues = [];
            for (let x = -10; x <= 10; x += 0.1) {
                xValues.push(x);
                data.labels.push(x.toFixed(1));
                data.datasets[0].data.push(equation(x));
            }

            const chartContainer = document.getElementById('chart-container');
            const chartCanvas = document.getElementById('chart');

            if (chart) {
                chart.data = data;
                chart.options.scales.x.min = Math.min(...xValues);
                chart.options.scales.x.max = Math.max(...xValues);
                chart.update();
            } else {
                const ctx = chartCanvas.getContext('2d');
                chart = new Chart(ctx, {
                    type: 'line',
                    data: data,
                    options: {
                        responsive: true,
                        scales: {
                            x: {
                                min: Math.min(...xValues),
                                max: Math.max(...xValues)
                            }
                        }
                    }
                });
            }
        }

        // Класи для вирішування нелінійних рівнянь
        class NonlinearEquationSolver {
            solve(equation, initialGuess, tolerance = 1e-6, maxIterations = 100) {
                throw new Error("Метод solve має бути реалізований у похідному класі");
            }
        }

        class NewtonRaphsonSolver extends NonlinearEquationSolver {
            solve(equation, initialGuess, tolerance = 1e-6, maxIterations = 100) {
                let x = initialGuess;
                let iterations = 0;

                const derivative = (f, x) => {
                    const h = 1e-6;
                    return (f(x + h) - f(x)) / h;
                };

                while (iterations < maxIterations) {
                    const fx = equation(x);
                    const dfx = derivative(equation, x);

                    if (Math.abs(dfx) < 1e-12) {
                        break;
                    }

                    const dx = -fx / dfx;
                    x += dx;

                    if (Math.abs(dx) < tolerance) {
                        return x;
                    }

                    iterations++;
                }

                return x;
            }
        }

        class SecantSolver extends NonlinearEquationSolver {
            solve(equation, initialGuess, tolerance = 1e-6, maxIterations = 100) {
                let x0 = initialGuess;
                let x1 = x0 + 0.1;
                let iterations = 0;

                while (iterations < maxIterations) {
                    const fx0 = equation(x0);
                    const fx1 = equation(x1);

                    if (Math.abs(fx1 - fx0) < 1e-12) {
                        break;
                    }

                    const x2 = x1 - fx1 * (x1 - x0) / (fx1 - fx0);

                    if (Math.abs(x2 - x1) < tolerance) {
                        return x2;
                    }

                    x0 = x1;
                    x1 = x2;
                    iterations++;
                }

                return x1;
            }
        }

        class BisectionSolver extends NonlinearEquationSolver {
            solve(equation, a, b, tolerance = 1e-6, maxIterations = 100) {
                let iterations = 0;

                if (equation(a) * equation(b) >= 0) {
                    console.error("Інтервал не містить коренів");
                    return null;
                }

                while (iterations < maxIterations) {
                    const c = (a + b) / 2;
                    const fc = equation(c);

                    if (Math.abs(fc) < tolerance) {
                        return c;
                    }

                    if (equation(a) * fc < 0) {
                        b = c;
                    } else {
                        a = c;
                    }

                    iterations++;
                }

                return (a + b) / 2;
            }
        }

        // Функція для показу вмісту
        function showContent(contentId) {
            const contents = document.getElementsByClassName("content");
            for (let i = 0; i < contents.length; i++) {
                contents[i].style.display = "none";
            }
            document.getElementById(contentId).style.display = "block";
        }

        // Обробники подій для кнопок навігації
        document.getElementById("catalog-btn").addEventListener("click", function () {
            showContent("catalog-content");
        });

        document.getElementById("antiviruses-btn").addEventListener("click", function () {
            showContent("antiviruses-content");
        });

        document.getElementById("os-btn").addEventListener("click", function () {
            showContent("os-content");
        });

        document.getElementById("office-btn").addEventListener("click", function () {
            showContent("office-content");
        });

        document.getElementById("utilities-btn").addEventListener("click", function () {
            showContent("utilities-content");
        });

        document.getElementById("delivery-btn").addEventListener("click", function () {
            showContent("delivery-content");
        });

        document.getElementById("payment-btn").addEventListener("click", function () {
            showContent("payment-content");
        });

        document.getElementById("equation-btn").addEventListener("click", function () {
            showContent("equation-content");
        });
    </script>
</body>
</html>
