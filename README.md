# EmailJs-Youtube-Tutorial

Link to video: 

There are multiple methods to getting emails to send through React. You can use Nodemailer, use express backend methods and so many others. 

We are going to be using EmailJs!

**This does not include saving information via form to your backend**

Service we are using: https://www.emailjs.com/

Step 1: Go to https://www.emailjs.com/ and create a free account.
Step 2: Once you have created an account you will need to connect your email service. I have only used Gmail and I have only tested using gmail.
Step 3: Now you will want to click "Email Templates" on the left side and then click "Create new template". After formatting your template be sure to enter your email on the right side under "To email". Click Test if you want to send a test email or click save.
Step 4: Go back to https://www.emailjs.com/ and click docs at the top
Step 5: After clicking docs scroll down to "Examples" and click React
Step 6: Lines of code to copy are...
        1. import emailjs from "emailjs-com";
        2.  function sendEmail(e) {
              e.preventDefault();
             emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', e.target, 'YOUR_USER_ID')
              .then((result) => {
                console.log(result.text);
              }, (error) => {
                console.log(error.text);
              });
            }

Step 6. We need to fill out the 3 of 4 parameters after sendForm. Pro-tip if you hover over sendForm in your code editor it will tell you what they paramerters mean.
        1. "YOUR_SERVICE_ID" this is the type of email server you are using
        2. "YOUR_TEMPLATE_ID" this is the templateID when you create a template within the EmailJs website.
        3. e.target is related to what the user is typing through your form, leave this one alone.
        4. "YOUR_USER_ID" is your API Key to get to this you need to click on your name in the top right, in my instance it was "Michael Remy" after clicking your name you will then click on "API KEYS" then you want to copy your User ID:
Step 7. That's it! If you created your React form correctly and you are calling the function "sendEmail" on your form onSubmit then your templated email should be sent to you!

I hope you find this very helpful in being able to send emails to yourself through React.
