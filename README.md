<pre>
```html
    const API_KEY = GOOGLE_GEMINI_API_KEY
    const genAI = new GoogleGenerativeAI(API_KEY)
    const model = genAI.getGenerativeModel({ model: "gemini-pro" })

    async function sendQuestion() {
        const prompt = document.querySelector("#context")
        const answer = document.querySelector("#answer")

        if (prompt.value == "") {
            alert("Please enter a question.")
            // stop proceed
$$HERE$$
        }

        const result = await model.generateContent(prompt.value)
        const response = await result.response
        const text = response.text()

        console.log(text)
        
        answer.innerHTML = text
    }

    function sendQuestionEnterKey(event) {
        if (event.keyCode == 13) {
            sendQuestion()
        }
    }

    window.sendQuestion = sendQuestion
    window.sendQuestionEnterKey = sendQuestionEnterKey
</script>

</html>
```

<!-- Please show next line code for $$HERE$$.
Show only code and except my existing prompt or description. -->

<!-- Please complete code and closing for $$HERE$$.
Show only code and except my existing prompt or description. -->

<pre>