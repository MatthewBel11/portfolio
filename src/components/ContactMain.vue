<template>
    <div class="wrapper">
      <h2 id="contact" class="contact">Contact Me</h2>
  
      <form action="https://formspree.io/f/xeqyzerl" method="post">
        <div class="inputName">
          <input  placeholder = 'Name' name="Name" id="name" type="text" required>
        </div>
  
        <div class="inputEmail">
          <input placeholder = 'Email' name="Email" id="email" type="email" required>
        </div>
  
        <div class="inputMessage">
          <textarea  placeholder = 'Message' name="Message" id="message" style="height: 300px;" required></textarea>
        </div>
  
        <div class="sendForm">
          <button type="submit" class="sendButton">Send</button>
        </div>
      </form>
    </div>
  </template>
  
  
  <style scoped>
    .wrapper {
      height: 100vh;
      display: flex;
      margin: 0 auto;
      flex-direction: column;
      text-align: center;
      color: azure;
      padding: 20px;
    }
  
    .contact {
      color: azure;
    }
  
    form {
      display: flex;
      flex-direction: column;
    }
  
    .inputName,
    .inputEmail,
    .inputMessage {
      margin-bottom: 10px;
    }
  
    label {
      color: white;
      margin-bottom: 5px;
    }
  
    input,
    textarea {
      width: 40%;
      padding: 10px;
      border-radius: 5px;
      border: 1px solid azure;
      box-sizing: border-box;
      background-color: #131313;
      color: azure;
    }
  
    .inputMessage textarea {
      height: 300px;
    }
  
    .sendForm {
      margin-top: 10px;
    }
  
    .sendButton {
    width: 40%;
      padding: 10px;
      border: 1px solid azure;
      background-color: #131313;
      color: azure;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease, transform 0.3s ease;
    }
  
    .sendButton:hover {
      background-color: #2779bd;
      transform: scale(1.05);
    }

    @media screen and (max-width: 900px){
        input,
        textarea,
        .sendButton
        {
            min-width: 270px;
        }
    }
  </style>