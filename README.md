# 40th-birthday
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surprise Birthday Trip to Paris!</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
</head>
<body class="bg-rose-100">
    <div id="root"></div>

    <script type="text/babel">
    function TripSurpriseReveal() {
        const [isRevealed, setIsRevealed] = React.useState(false);

        const tripDetails = {
            destination: 'Paris, France',
            dates: 'October 5-12, 2024',
            highlights: [
                'Eiffel Tower private evening tour',
                'Gourmet food and wine walking tour', 
                'Day trip to Versailles',
                'Seine River sunset cruise',
                'Exclusive cooking class with a local chef'
            ]
        };

        return (
            <div className="min-h-screen flex items-center justify-center p-4">
                <div className="bg-white shadow-2xl rounded-2xl max-w-md w-full p-6 text-center">
                    {!isRevealed ? (
                        <div>
                            <h1 className="text-2xl font-bold text-gray-800 mb-4">
                                A Special Surprise Awaits!
                            </h1>
                            <button 
                                onClick={() => setIsRevealed(true)}
                                className="bg-rose-500 hover:bg-rose-600 text-white font-bold py-3 px-6 rounded-full"
                            >
                                Reveal Surprise
                            </button>
                        </div>
                    ) : (
                        <div>
                            <h1 className="text-3xl font-bold text-rose-800 mb-2">
                                40 & Fabulous in Paris!
                            </h1>
                            <div className="space-y-4 text-left">
                                <div className="bg-rose-50 p-3 rounded-lg">
                                    <h3 className="font-bold">Destination</h3>
                                    <p>{tripDetails.destination}</p>
                                </div>
                                <div className="bg-rose-50 p-3 rounded-lg">
                                    <h3 className="font-bold">Dates</h3>
                                    <p>{tripDetails.dates}</p>
                                </div>
                                <div className="bg-rose-50 p-3 rounded-lg">
                                    <h3 className="font-bold">Highlights</h3>
                                    <ul className="list-disc list-inside">
                                        {tripDetails.highlights.map((highlight, index) => (
                                            <li key={index}>{highlight}</li>
                                        ))}
                                    </ul>
                                </div>
                            </div>
                        </div>
                    )}
                </div>
            </div>
        );
    }

    ReactDOM.render(<TripSurpriseReveal />, document.getElementById('root'));
    </script>
</body>
</html>
```