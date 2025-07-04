import React, { useEffect, useState } from 'react';

function GmailClient() {
  const [emails, setEmails] = useState([]);

  useEffect(() => {
    // Simulated emails – replace with real Gmail API logic
    setEmails([
      { subject: 'Welcome to Gmail API', from: 'noreply@gmail.com' },
      { subject: 'Your application update', from: 'careers@mbzuai.ac.ae' }
    ]);
  }, []);

  return (
    <div style={{ padding: '2rem' }}>
      <h2>📧 Gmail Client</h2>
      <ul>
        {emails.map((email, index) => (
          <li key={index}>
            <strong>From:</strong> {email.from}<br />
            <strong>Subject:</strong> {email.subject}
          </li>
        ))}
      </ul>
    </div>
  );
}

export default GmailClient;

