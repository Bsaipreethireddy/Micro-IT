from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return '''
    <html>
    <head>
        <title>My Portfolio</title>
        <style>
            body { font-family: Arial; background-color: #f0f0f0; padding: 20px; }
            nav a { margin: 10px; text-decoration: none; color: #333; }
        </style>
    </head>
    <body>
        <h1>Welcome to My Portfolio</h1>
        <nav>
            <a href="/">Home</a> |
            <a href="/about">About Me</a> |
            <a href="/projects">Projects</a> |
            <a href="/contact">Contact</a>
        </nav>
        <p>This is a portfolio made for my MITS Internship.</p>
    </body>
    </html>
    '''

@app.route('/about')
def about():
    return '''
    <html>
    <head><title>About Me</title></head>
    <body>
        <h2>About Me</h2>
        <p>I am a BTech student with a passion for Python, Web Development, and Machine Learning.</p>
        <a href="/">Back to Home</a>
    </body>
    </html>
    '''

@app.route('/projects')
def projects():
    return '''
    <html>
    <head><title>Projects</title></head>
    <body>
        <h2>Projects</h2>
        <ul>
            <li>Medicine Recommendation System using ML</li>
            <li>Student Result Analyzer</li>
            <li>Web-based Calculator</li>
        </ul>
        <a href="/">Back to Home</a>
    </body>
    </html>
    '''

@app.route('/contact')
def contact():
    return '''
    <html>
    <head><title>Contact</title></head>
    <body>
        <h2>Contact</h2>
        <p>Email: yourname@example.com</p>
        <p>LinkedIn: <a href="https://linkedin.com/in/yourprofile">linkedin.com/in/yourprofile</a></p>
        <a href="/">Back to Home</a>
    </body>
    </html>
    '''

if __name__ == '__main__':
    app.run(debug=True)
