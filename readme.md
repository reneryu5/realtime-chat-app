# Real Time Chat App With React JS and Appwrite

A chat app with real-time capabilities that utilizes Appwrite on the backend.

🎥 [Tutorial Link](https://youtu.be/t7S0I78sloI?feature=shared)

<img src="images/demo.png"/>

### Getting Started

After cloning the repo ensure you complete the necessary installations

```
$ npm install
$ npm run dev
```

Create a new `.env` folder and create the necessary variables based on the `src/appwriteConfig.js` file. Appwrite setup will be covered in the next step.

```js
//appwrite.Config.js
...
export const API_ENDPOINT = import.meta.env.VITE_API_ENDPOINT
export const PROJECT_ID = import.meta.env.VITE_PROJECT_ID
export const DATABASE_ID = import.meta.env.VITE_DATABASE_ID
export const COLLECTION_ID_MESSAGES = import.meta.env.VITE_COLLECTION_ID_MESSAGES

const client = new Client()
    .setEndpoint(API_ENDPOINT)
    .setProject(PROJECT_ID);
...
```

**Setting Up Appwrite Account**

Set up a local instance of Appwrite or create an account with Appwrite Cloud.

In your appwrite console create a project and database.

1. Create a collection called "messages" and add the following attributes:
 <table>
     <tr>
         <th>Atrtibute Name</th>
         <th>Type</th>
         <th>Size</th>
     </tr>
         <tr>
         <td>user_id</td>
         <td>string</td>
         <td>50</td>
     </tr>
         </tr>
         <tr>
         <td>username</td>
         <td>string</td>
         <td>50</td>
     </tr>
         </tr>
         <tr>
         <td>body</td>
         <td>string</td>
         <td>250</td>
     </tr>
 </table>
2. From your `messages` collection, go to the "settings" --> "Update Permissions" --> "+ Add Role" and select "Any". Give this user type "Create", "Read", "Update" and "Delete" permissions.

Once you've set up your project you should be able to update all necessary env variables.
Run your development server to view the output.
