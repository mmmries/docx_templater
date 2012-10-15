Word Templater
==============

Use .docx as reusable templates
   
Example usage:
     buffer = WordTemplater.replace_file_with_content('path/to/mydocument.docx',
        {
          :client_email1 => 'test@example.com',
          :client_phone1 => '555-555-5555',
        })
     # In Rails you can send a word document via send_data
     send_data buffer.string, :filename => 'REPC.docx'
     # Or save the output to a word file
     File.open("path/to/mydocument.docx", "wb") {|f| f.write(buffer.string) }