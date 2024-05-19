# CS361_Microservice

This microservice allows users to upload files through a web interface and saves them to an upload directory. The service is built using Flask and provides endpoints for file uploads and status checks. A user can also submit a file through the terminal using the curl command.

<h1>Setup Instructions</h1>

<ol>
  <li><h3>Clone the Repository</h3>
  <ul>
    <li>git clone https://github.com/your-username/CS361_Microservice.git</li>
    <li>cd CS361_Microservice</li>
  </ul>
  </li>

  <li><h3>Run the Application</h3>
   <ul>
      <li>python3 file_upload.py
  </li>
  </ul>
  </li>
</ol>

<h1>Requesting Data</h1>
<h2>Ensure the server is running!</h2>
<ol>
  <li><h3>Through Localhost, *port 8000 default</h3>
  <ul>
    <li>Choose a file using the file browser</li>
    <li>Click the upload button</li>
  </ul>
  </li>

   <li><h3>Through your terminal</h3>
  <ul>
    <h4>Use this command replacing "@/path/to/your/file.txt" with the path to your file.
    <ul>
       <li>curl -F "file=@/path/to/your/file.txt" http://127.0.0.1:8000/upload
</li>
    </ul>
    </h4>
    
  </ul>
  </li>
</ol>


<h1>Receiving Data</h1>

<ol>
  <li><h3>Through the Localhost and the terminal, JSON data will be returned!</h3>
  <ul>
    <li>After uploading a file, you will receive one of three messages:
      <h4>Success
      <ul>
      <li>{
    "message": "File uploaded successfully!",
    "filename": "file.txt"
    }</li>
      </ul>
      </h4>
       <h4>Failure
      <ul>
      <li>{
    "error": "Error uploading file!"
}</li>
      </ul>
      </h4>
       <h4>Error
      <ul>
      <li>{
    "message": "File type not allowed!",
    "filename": "file.txt"
    }</li>
      </ul>
      </h4>
    </li>
    
  </ul>
  </li>
    </h4>
    
  </ul>
  </li>
</ol>
<h1>UML Sequence Diagram</h1>
![uml-sequence-diagram-example](https://github.com/gChrisj/CS361_Microservice/blob/main/uml-sequence-diagram.png?raw=true)

