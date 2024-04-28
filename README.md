## <a href="https://ilostmyipad.web.app">iLostmyipad.web.app</a>
<img width="1170" alt="Screenshot 2024-04-27 at 11 52 51 PM" src="https://github.com/sudo-self/react-firebase-photos/assets/119916323/85d445f5-57f6-42d0-8432-bfd18848e85c"><hr>
Bucket Rules<br>
rules_version = '2';
service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      // Allow read access to all users
      allow read: if true;
      allow write: if request.auth != null;
    }
  }
}
