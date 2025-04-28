# AssignCheck - AI-Powered Assignment Evaluation System

AssignCheck is an intelligent system for evaluating student assignments using AI-powered analysis to detect plagiarism, assess relevance, and generate comprehensive feedback.

## Core Features

### 1. Answer Comparison (Relevance Checking)

The system compares student answers with the teacher's answer key using AI-based semantic similarity:

- **Semantic Analysis**: Utilizes AI language models to understand the meaning of answers, not just keyword matching
- **Relevance Percentage**: Generates a score from 0-100% indicating how closely the student's answer matches the expected concepts
- **Detailed Explanation**: Provides insights on why an answer received a specific relevance score

### 2. Plagiarism Detection

Automatically checks student submissions for potential plagiarism:

- **Content Matching**: Compares submitted text against a database of academic sources
- **Plagiarism Percentage**: Calculates a score indicating how much of the submission matches existing content
- **Source Identification**: Lists the specific sources that match the student's submission

### 3. Weighted Scoring System

Combines relevance and originality into a comprehensive evaluation:

```
Final Score (%) = (Relevance % * 0.8) + ((100 - Plagiarism %) * 0.2)
```

Example calculation:
- Relevance Score: 85%
- Plagiarism Score: 10%
- Final Score: (85 * 0.8) + (90 * 0.2) = 68 + 18 = 86%

### 4. Comprehensive Reports

Generate detailed evaluation reports for students and teachers:

- Overall scores and metrics
- Question-by-question breakdown
- Plagiarism analysis
- Detailed feedback on each answer
- Downloadable PDF format

## Technical Implementation

### Service Architecture

- **OpenAI Service**: Handles semantic comparison between student and teacher answers
- **Plagiarism Service**: Analyzes text for matches against external sources
- **Performance Service**: Processes evaluation results and calculates final scores
- **PDF Service**: Generates downloadable reports with detailed analysis

### Integration Instructions

To integrate the system with existing assignments:

1. **Teacher Setup**:
   - Create assignments with detailed answer keys
   - Specify scoring weights for each question if needed

2. **Student Submission**:
   - Submit answers through the platform interface
   - Receive immediate preliminary feedback

3. **Evaluation Process**:
   - System automatically processes submissions
   - Calculates relevance through AI comparison
   - Performs plagiarism checking
   - Generates weighted final scores
   - Creates comprehensive feedback

4. **Accessing Results**:
   - Students: View scores and feedback through the dashboard
   - Teachers: Access detailed analysis of class performance
   - Both: Download PDF reports for records

## Demo System Notes

This demo implementation includes simulated versions of the AI and plagiarism checking services. In a production environment, these would be connected to actual APIs:

- **OpenAI API**: For the semantic text comparison
- **Grammarly or similar API**: For detailed plagiarism detection

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Developed for educational technology applications
- Uses modern AI techniques for natural language understanding
- Designed to promote academic integrity and meaningful feedback 