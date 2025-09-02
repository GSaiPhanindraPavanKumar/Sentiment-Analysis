# Sentiment Analysis Web Application

A Flask-based web application that performs sentiment analysis on user-provided text using VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analysis tool.

## Features

- **Real-time Sentiment Analysis**: Analyze the sentiment of any text input
- **Detailed Scoring**: Get comprehensive sentiment scores including:
  - Positive sentiment score
  - Negative sentiment score  
  - Neutral sentiment score
  - Compound sentiment score
- **User-friendly Interface**: Clean web interface with background styling
- **Text Preprocessing**: Automatic text cleaning including:
  - Conversion to lowercase
  - Removal of digits
  - Removal of English stopwords

## Technology Stack

- **Backend**: Flask (Python web framework)
- **Sentiment Analysis**: VADER Sentiment Analyzer
- **Text Processing**: NLTK (Natural Language Toolkit)
- **Machine Learning**: scikit-learn (TfidfVectorizer, cosine_similarity)
- **Frontend**: HTML, CSS
- **Styling**: Custom CSS with background image

## Project Structure

```
Sentiment-Analysis/
├── app.py                 # Main Flask application
├── templates/
│   └── form.html         # HTML template for the web interface
├── static/
│   ├── style.css         # Custom CSS styles
│   └── Background.png    # Background image
└── img/                  # Image assets directory
```

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/GSaiPhanindraPavanKumar/Sentiment-Analysis.git
   cd Sentiment-Analysis
   ```

2. **Install required dependencies**:
   ```bash
   pip install flask
   pip install scikit-learn
   pip install vaderSentiment
   pip install nltk
   ```

3. **Download NLTK data** (required for stopwords):
   ```python
   import nltk
   nltk.download('stopwords')
   ```

## Usage

1. **Run the application**:
   ```bash
   python app.py
   ```

2. **Access the web interface**:
   - Open your web browser
   - Navigate to `http://127.0.0.1:5002`

3. **Analyze sentiment**:
   - Enter your text in the textarea
   - Click the submit button
   - View the detailed sentiment analysis results

## How It Works

1. **Text Preprocessing**:
   - User input is converted to lowercase
   - Digits are removed from the text
   - English stopwords are filtered out

2. **Sentiment Analysis**:
   - Processed text is analyzed using VADER sentiment analyzer
   - VADER provides polarity scores for positive, negative, neutral, and compound sentiment

3. **Results Display**:
   - Sentiment scores are displayed in a formatted table
   - Overall sentiment percentage is calculated and shown

## API Endpoints

- `GET /`: Displays the sentiment analysis form
- `POST /`: Processes the submitted text and returns sentiment analysis results

## Configuration

- **Host**: 127.0.0.1 (localhost)
- **Port**: 5002
- **Debug Mode**: Enabled for development
- **Threading**: Enabled for concurrent requests

## Dependencies

- `Flask`: Web framework
- `scikit-learn`: Machine learning library (TfidfVectorizer, cosine_similarity)
- `vaderSentiment`: Sentiment analysis tool
- `nltk`: Natural language processing library
- `string`: Built-in Python module for string operations
- `re`: Built-in Python module for regular expressions

## Sample Output

When you input text like "I love this application!", you'll get:

- **Positive**: 0.746
- **Neutral**: 0.254
- **Negative**: 0.000
- **Compound**: 0.6696
- **Overall Sentiment**: ~83% positive

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Create a Pull Request

## Future Enhancements

- [ ] Add support for multiple languages
- [ ] Implement batch text analysis
- [ ] Add data visualization for sentiment trends
- [ ] Include emotion detection alongside sentiment
- [ ] Add API endpoints for programmatic access
- [ ] Implement user authentication and history
- [ ] Add export functionality for results

## License

This project is open source and available under the [MIT License](LICENSE).

## Author

**GSaiPhanindraPavanKumar**
- GitHub: [@GSaiPhanindraPavanKumar](https://github.com/GSaiPhanindraPavanKumar)

## Acknowledgments

- VADER Sentiment Analysis tool
- Flask framework community
- NLTK developers
- scikit-learn contributors
