<script>
    import { onMount } from 'svelte';
    import { marked } from 'marked';
    import 'prismjs/themes/prism.css'; // Optional: Import Prism.js theme for code highlighting
  
    let markdownContent = ''; // Initialize as an empty string
  
    onMount(async () => {
      const response = await fetch('/webpage-design.md'); // Fetch the Markdown content from the file
      markdownContent = await response.text(); // Set markdownContent to the fetched content
    });
  </script>
  
  <div class="markdown-content" innerHTML={marked(markdownContent)}></div>
  
  <style>
    /* Ensure the markdown container is responsive */
    .markdown-content {
      max-width: 800px;
      margin: 0 auto;
      padding: 20px;
      font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
      line-height: 1.6;
      word-wrap: break-word; /* Handle long words and URLs */
    }
  
    /* Headings styling */
    .markdown-content h1,
    .markdown-content h2,
    .markdown-content h3 {
      margin-top: 1.2em;
      margin-bottom: 0.5em;
      font-weight: bold;
      line-height: 1.25;
    }
  
    .markdown-content h1 {
      font-size: 2.5em;
    }
  
    .markdown-content h2 {
      font-size: 2em;
    }
  
    .markdown-content h3 {
      font-size: 1.75em;
    }
  
    /* Paragraph styling */
    .markdown-content p {
      margin-bottom: 1em;
    }
  
    /* Code block styling */
    .markdown-content pre {
      background-color: #f4f4f4;
      padding: 15px;
      border-radius: 5px;
      overflow-x: auto; /* Allow horizontal scrolling on small screens */
    }
  
    .markdown-content code {
      background-color: #f4f4f4;
      padding: 2px 4px;
      border-radius: 3px;
      font-family: 'Courier New', Courier, monospace;
    }
  
    /* Lists styling */
    .markdown-content ul,
    .markdown-content ol {
      padding-left: 1.5em;
      margin-bottom: 1em;
    }
  
    /* Table styling */
    .markdown-content table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 1em;
    }
  
    .markdown-content table,
    .markdown-content th,
    .markdown-content td {
      border: 1px solid #ddd;
      padding: 8px;
    }
  
    .markdown-content th {
      background-color: #f8f8f8;
      font-weight: bold;
    }
  
    .markdown-content tr:nth-child(even) {
      background-color: #f9f9f9;
    }
  
    /* Image styling */
    .markdown-content img {
      max-width: 100%; /* Ensure images are responsive */
      height: auto;
      display: block;
      margin: 1em auto; /* Center images */
    }
  
    /* Link styling */
    .markdown-content a {
      color: #007bff;
      text-decoration: none;
      border-bottom: 1px solid transparent;
      transition: all 0.3s ease;
    }
  
    .markdown-content a:hover {
      color: #0056b3;
      border-bottom-color: #0056b3;
    }
  
    /* Responsive design */
    @media (max-width: 600px) {
      .markdown-content {
        padding: 15px;
      }
  
      .markdown-content h1 {
        font-size: 1.8em;
      }
  
      .markdown-content h2 {
        font-size: 1.5em;
      }
  
      .markdown-content h3 {
        font-size: 1.3em;
      }
  
      .markdown-content table,
      .markdown-content th,
      .markdown-content td {
        font-size: 0.9em;
        padding: 6px;
      }
    }
  </style>
  