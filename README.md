<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Survey Form</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background: white;
            border-radius: 10px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
            padding: 40px;
            max-width: 600px;
            width: 100%;
        }

        h1 {
            color: #333;
            margin-bottom: 10px;
            text-align: center;
        }

        .subtitle {
            color: #666;
            text-align: center;
            margin-bottom: 30px;
            font-size: 14px;
        }

        .form-group {
            margin-bottom: 25px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #333;
            font-weight: 500;
            font-size: 14px;
        }

        .required {
            color: #e74c3c;
        }

        input[type="text"],
        input[type="email"],
        input[type="number"],
        textarea,
        select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 14px;
            font-family: inherit;
            transition: border-color 0.3s;
        }

        input[type="text"]:focus,
        input[type="email"]:focus,
        input[type="number"]:focus,
        textarea:focus,
        select:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 5px rgba(102, 126, 234, 0.1);
        }

        textarea {
            resize: vertical;
            min-height: 100px;
        }

        .radio-group,
        .checkbox-group {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .radio-item,
        .checkbox-item {
            display: flex;
            align-items: center;
        }

        input[type="radio"],
        input[type="checkbox"] {
            margin-right: 10px;
            width: 18px;
            height: 18px;
            cursor: pointer;
        }

        .radio-item label,
        .checkbox-item label {
            margin-bottom: 0;
            cursor: pointer;
            font-weight: 400;
        }

        .button-group {
            display: flex;
            gap: 10px;
            margin-top: 30px;
        }

        button {
            flex: 1;
            padding: 12px 20px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }

        .submit-btn {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(102, 126, 234, 0.4);
        }

        .reset-btn {
            background: #ecf0f1;
            color: #333;
        }

        .reset-btn:hover {
            background: #d5dbdb;
        }

        .success-message {
            display: none;
            background: #d4edda;
            color: #155724;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 20px;
            border: 1px solid #c3e6cb;
        }

        .error-message {
            color: #e74c3c;
            font-size: 12px;
            margin-top: 5px;
            display: none;
        }

        .form-group.error input,
        .form-group.error textarea,
        .form-group.error select {
            border-color: #e74c3c;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="success-message" id="successMessage">
            ✓ Thank you! Your survey has been submitted successfully.
        </div>

        <h1>Is Intersession For UNO?</h1>
        <p class="subtitle">Your feedback helps keep the focus on students. Thank you!</p>

        <form id="surveyForm">

            <!-- Select Dropdown -->
            <div class="form-group">
                <label for="Colleges">What are you majoring in? <span class="required">*</span></label>
                <select id="department" name="department" required>
                    <option value="">-- Select an option --</option>
                    <option value="sales">Arts and Science</option>
                    <option value="support">Buisness</option>
                    <option value="product">Communication and Fine Arts</option>
                    <option value="product">Information Science and Technology</option>
                    <option value="engineering">Public Affairs and Community Service</option>
                    <option value="other">Other</option>
                </select>
                <div class="error-message">Please select a department</div>
            </div>

<!-- Select Dropdown -->
<div class="form-group">
    <label for="year">
        How many years have you attended UNO 
        <span class="required">*</span>
    </label>

    <select id="year" name="year" required>
        <option value="">-- Select an option --</option>
        <option value="1">1 year or less</option>
        <option value="2">2 years</option>
        <option value="3">3 years</option>
        <option value="4+">4 or more years</option>
    </select>

    <div class="error-message">Please select a value</div>
</div>
            
<div class="form-group">
    <label>
       Do you know what intersession classes are?
        <span class="required">*</span>
    </label>

    <div class="radio-group">
        <div class="radio-item">
            <input type="radio" id="trueOption" name="educationQuality" value="Yes" required>
            <label for="trueOption">Yes</label>
        </div>

        <div class="radio-item">
            <input type="radio" id="falseOption" name="educationQuality" value="No">
            <label for="falseOption">No</label>
        </div>
    </div>

    <div class="error-message">Please select one option</div>
</div>

<div class="form-group">
    <label>
       Did you know that intercession classes have replaced the J term
        <span class="required">*</span>
    </label>

    <div class="radio-group">
        <div class="radio-item">
            <input type="radio" id="trueOption" name="educationQuality" value="Yes" required>
            <label for="trueOption">Yes</label>
        </div>

        <div class="radio-item">
            <input type="radio" id="falseOption" name="educationQuality" value="No">
            <label for="falseOption">No</label>
        </div>
    </div>

    <div class="error-message">Please select one option</div>
</div>

            <!-- Radio Buttons -->
            <div class="form-group">
                <label>Are you interested in taking a intersession class?<span class="required">*</span></label>
                <div class="radio-group">
                    <div class="radio-item">
                        <input type="radio" id="interested" name="interested" value="interested">
                        <label for="interested">Interested</label>
                    </div>
                    <div class="radio-item">
                        <input type="radio" id="neutral" name="interested" value="neutral">
                        <label for="neutral">Neutral</label>
                    </div>
                    <div class="radio-item">
                        <input type="radio" id="uninterested" name="interested" value="uninterested">
                        <label for="uninterested">Uninterested</label>
                    </div>
                </div>
                <div class="error-message">Please select an option</div>
            </div>

            <!-- Checkboxes -->
            <div class="form-group">
                <label>Do you or have you used J term for classes? <span class="required">*</span></label>
                <div class="checkbox-group">
                    <div class="checkbox-item">
                        <input type="checkbox" id="feature1" name="features" value="I have and it was helpful">
                        <label for="feature1">I have and it was helpful</label>
                    </div>
                    <div class="checkbox-item">
                        <input type="checkbox" id="feature2" name="features" value="I have not but I was hoping to">
                        <label for="feature2">I have not but I was hoping to</label>
                    </div>
                    <div class="checkbox-item">
                        <input type="checkbox" id="feature3" name="features" value="I have not and I did not plan to">
                        <label for="feature3">I have not and I did not plan to</label>
                    </div>
                    <div class="checkbox-item">
                        <input type="checkbox" id="feature4" name="features" value="I have and it was not helpful">
                        <label for="feature4">I have and it was not helpful</label>
                    </div>
                </div>
                <div class="error-message">Please select at least one feature</div>
            </div>
<div class="form-group">
    <label>
        I would receive quality education in the 10 - 14 days for a 3-credit class.
        <span class="required">*</span>
    </label>

    <div class="radio-group">
        <div class="radio-item">
            <input type="radio" id="trueOption" name="educationQuality" value="True" required>
            <label for="trueOption">True</label>
        </div>

        <div class="radio-item">
            <input type="radio" id="falseOption" name="educationQuality" value="False">
            <label for="falseOption">False</label>
        </div>
    </div>

    <div class="error-message">Please select one option</div>
</div>
            <!-- Radio Buttons -->
            <div class="form-group">
                <label>Do you think 10-14 days intersession class would provide the same quality education as the 3 week J term.<span class="required">*</span></label>
                <div class="radio-group">
                    <div class="radio-item">
                        <input type="radio" id="agree" name="interested" value="agree">
                        <label for="agree">Agree</label>
                    </div>
                    <div class="radio-item">
                        <input type="radio" id="neutral" name="interested" value="neutral">
                        <label for="neutral">Neutral</label>
                    </div>
                    <div class="radio-item">
                        <input type="radio" id="disagree" name="disagree" value="disagree">
                        <label for="disagree">Disagree</label>
                    </div>
                </div>
            <!-- Textarea -->
            <div class="form-group">
                <label for="comments">Additional Comments</label>
                <textarea id="comments" name="comments" placeholder="Share any additional feedback or suggestions..."></textarea>
            </div>

            <!-- Checkbox for terms -->
            <div class="form-group">
                <div class="checkbox-item">
                    <input type="checkbox" id="terms" name="terms" required>
                    <label for="terms">I agree to share my feedback <span class="required">*</span></label>
                </div>
                <div class="error-message">You must agree to proceed</div>
            </div>

               <!-- Text Input -->
            <div class="form-group">
                <label for="name">Full Name <span class="required">*</span></label>
                <input type="text" id="name" name="name" placeholder="Enter your name" required>
                <div class="error-message">Please enter your name</div>
            </div>

            <!-- Email Input -->
            <div class="form-group">
                <label for="email">Email Address <span class="required">*</span></label>
                <input type="email" id="email" name="email" placeholder="Enter your email" required>
                <div class="error-message">Please enter a valid email</div>
            </div>

            <!-- Buttons -->
            <div class="button-group">
                <button type="submit" class="submit-btn">Submit Survey</button>
                <button type="reset" class="reset-btn">Clear Form</button>
            </div>
        </form>
    </div>

    <script>
        const form = document.getElementById('surveyForm');
        const successMessage = document.getElementById('successMessage');

        form.addEventListener('submit', function(e) {
            e.preventDefault();

            // Clear previous error messages
            document.querySelectorAll('.form-group').forEach(group => {
                group.classList.remove('error');
                const errorMsg = group.querySelector('.error-message');
                if (errorMsg) errorMsg.style.display = 'none';
            });

            // Validate form
            let isValid = true;

            // Validate required text inputs
            const name = document.getElementById('name');
            if (!name.value.trim()) {
                showError(name);
                isValid = false;
            }

            // Validate email
            const email = document.getElementById('email');
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(email.value)) {
                showError(email);
                isValid = false;
            }

            // Validate select
            const department = document.getElementById('department');
            if (!department.value) {
                showError(department);
                isValid = false;
            }

            // Validate radio buttons
            const satisfactionChecked = document.querySelector('input[name="satisfaction"]:checked');
            if (!satisfactionChecked) {
                const radioGroup = document.querySelector('input[name="satisfaction"]').closest('.form-group');
                radioGroup.classList.add('error');
                const errorMsg = radioGroup.querySelector('.error-message');
                if (errorMsg) errorMsg.style.display = 'block';
                isValid = false;
            }

            // Validate checkboxes (at least one)
            const featuresChecked = document.querySelectorAll('input[name="features"]:checked');
            if (featuresChecked.length === 0) {
                const checkboxGroup = document.querySelector('input[name="features"]').closest('.form-group');
                checkboxGroup.classList.add('error');
                const errorMsg = checkboxGroup.querySelector('.error-message');
                if (errorMsg) errorMsg.style.display = 'block';
                isValid = false;
            }

            // Validate terms checkbox
            const terms = document.getElementById('terms');
            if (!terms.checked) {
                const termsGroup = terms.closest('.form-group');
                termsGroup.classList.add('error');
                const errorMsg = termsGroup.querySelector('.error-message');
                if (errorMsg) errorMsg.style.display = 'block';
                isValid = false;
            }

            // If valid, show success message and log data
            if (isValid) {
                // Collect form data
                const formData = new FormData(form);
                const data = {
                    name: formData.get('name'),
                    email: formData.get('email'),
                    department: formData.get('department'),
                    satisfaction: formData.get('satisfaction'),
                    features: formData.getAll('features'),
                    comments: formData.get('comments'),
                    timestamp: new Date().toISOString()
                };

                // Log to console (in a real app, you'd send this to a server)
                console.log('Survey Data:', data);

                // Show success message
                successMessage.style.display = 'block';

                // Reset form
                form.reset();

                // Hide success message after 5 seconds
                setTimeout(() => {
                    successMessage.style.display = 'none';
                }, 5000);
            }
        });

        function showError(element) {
            const formGroup = element.closest('.form-group');
            formGroup.classList.add('error');
            const errorMsg = formGroup.querySelector('.error-message');
            if (errorMsg) errorMsg.style.display = 'block';
        }
    </script>
</body>
</html>
