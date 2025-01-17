<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bathroom Cleaning Request</title>
</head>
<body>
    <h1>Bathroom Cleaning Service Request</h1>
    <p>Please fill out the form below to request a bathroom cleaning. Your response will be sent directly to our service team.</p>
    
    <form id="cleaningForm" onsubmit="submitForm(event)">
        <label for="location">Cleaning Location:</label><br>
        <input type="text" id="location" name="location" required><br><br>

        <label for="type">Type of Cleaning Needed:</label><br>
        <input type="text" id="type" name="type" required><br><br>

        <label for="contact">Your Phone Number (optional, if you'd like to be contacted):</label><br>
        <input type="tel" id="contact" name="contact" placeholder="123-456-7890"><br><br>

        <button type="submit">Submit</button>
    </form>

    <script>
        async function submitForm(event) {
            event.preventDefault();

            const location = document.getElementById('location').value;
            const type = document.getElementById('type').value;
            const contact = document.getElementById('contact').value;

            const message = `Cleaning Request:\nLocation: ${location}\nType: ${type}\nContact: ${contact || 'N/A'}`;

            try {
                await fetch('https://textbelt.com/text', {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({
                        phone: '8067869017',
                        message: message,
                        key: 'textbelt',
                    }),
                });

                alert('Your request has been sent successfully!');
                document.getElementById('cleaningForm').reset();
            } catch (error) {
                alert('There was an error sending your request. Please try again later.');
            }
        }
    </script>

    <footer>
        <p>Scan the QR code below to open this form on your phone:</p>
        <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://yourwebsite.com/bathroom-cleaning" alt="QR Code">
    </footer>
</body>
</html>
