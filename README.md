# Messenger Clone

Welcome to the Messenger Clone project! This is a real-time messaging application built using Next.js 13, React, Tailwind, Prisma, MongoDB, NextAuth, and Pusher. The project aims to provide a sleek and responsive user interface for messaging, supporting various features like real-time messaging, notifications, user authentication, file sharing, and more.

## Deployed App

[https://messenverse.vercel.app/](https://messenverse.vercel.app/)

## Screenshots

| Screenshot 1 | Screenshot 2 | Screenshot 3 |
| :---: | :---: | :---: |
| ![Screenshot 1](/public/images/ss01.png) | ![Screenshot 2](/public/images/ss02.png) | ![Screenshot 3](/public/images/ss03.png) |
| Screenshot 4 | Screenshot 5 |
| ![Screenshot 4](/public/images/ss04.png) | ![Screenshot 6](/public/images/ss05.png) |



## Main Features

### 1. Real-time Messaging using Pusher

The application leverages Pusher to enable real-time messaging between users, ensuring messages are delivered instantly.

### 2. Message Notifications and Alerts

Users receive notifications and alerts for new messages and other important events, keeping them informed at all times.

### 3. Tailwind Design for Sleek UI

The project utilizes Tailwind CSS to create a modern and visually appealing user interface.

### 4. Tailwind Animations and Transition Effects

Enhance the user experience with smooth animations and transition effects created using Tailwind CSS.

### 5. Full Responsiveness for All Devices

The application is designed and optimized to be fully responsive, allowing users to access and use it seamlessly on various devices.

### 6. Credential Authentication with NextAuth

User authentication is implemented using NextAuth, allowing users to sign up, log in, and manage their accounts securely.

### 7. Google Authentication Integration

Users have the option to sign in using their Google accounts, providing a convenient and quick login process.

### 8. Github Authentication Integration

For Github users, the project offers the option to authenticate using their Github accounts.

### 9. File and Image Upload using Cloudinary CDN

Users can upload files and images to the application using the Cloudinary CDN service, making it easy to share media.

### 10. Client Form Validation and Handling using react-hook-form

Form validation and handling on the client-side are managed using the powerful `react-hook-form` library.

### 11. Server Error Handling with react-toast

Error handling on the server-side is implemented with `react-toast`, providing clear and informative error messages to users.

### 12. Message Read Receipts

Users can see if their messages have been read by other recipients, providing insight into the message's status.

### 13. Online/Offline User Status

The application displays the online/offline status of users, making it easier to know who is currently active.

### 14. Group Chats and One-on-One Messaging

Users can participate in group chats or engage in one-on-one messaging, supporting various communication scenarios.

### 15. Message Attachments and File Sharing

Files and attachments can be shared within the messaging platform, allowing users to exchange various media types.

### 16. User Profile Customization and Settings

Users can customize their profiles and manage settings to personalize their experience.

### 17. Writing POST, GET, and DELETE Routes in Route Handlers (app/api)

The project includes examples and guides on writing various API routes to handle data interactions.

### 18. Fetching Data in Server React Components Directly from the Database (WITHOUT API!)

The project demonstrates how to fetch data directly from the database in server-side React components, without relying on APIs.

### 19. Handling Relations between Server and Child Components in a Real-time Environment

Learn how to manage and handle relations between server and child components in a real-time messaging environment.

### 20. Creating and Managing Chat Rooms and Channels

The application supports the creation and management of chat rooms and channels for different user groups.


### Prerequisites

**Node version 14.x**

### Cloning the repository

```shell
git clone https://github.com/khantseithu/messenger-clone.git
```

### Install packages

```shell
npm i
```

### Setup .env file


```js
DATABASE_URL=
NEXTAUTH_SECRET=

NEXT_PUBLIC_PUSHER_APP_KEY=
PUSHER_APP_ID=
PUSHER_SECRET=

NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=

GITHUB_ID=
GITHUB_SECRET=

GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
```

### Setup Prisma

```shell
npx prisma db push

```

### Start the app

```shell
npm run dev
```

## Available commands

Running commands with npm `npm run [command]`

| command         | description                              |
| :-------------- | :--------------------------------------- |
| `dev`           | Starts a development instance of the app |


## Folder Structure
```shell
.
├── LICENSE
├── README.md
├── app
│   ├── (site)
│   │   ├── components
│   │   │   ├── AuthForm.tsx
│   │   │   └── AuthSocialButton.tsx
│   │   └── page.tsx
│   ├── actions
│   │   ├── getConversationById.ts
│   │   ├── getConversations.ts
│   │   ├── getCurrentUser.ts
│   │   ├── getMessages.ts
│   │   ├── getSession.ts
│   │   └── getUsers.ts
│   ├── api
│   │   ├── auth
│   │   │   └── [...nextauth]
│   │   │       └── route.ts
│   │   ├── conversations
│   │   │   ├── [conversationId]
│   │   │   │   ├── route.ts
│   │   │   │   └── seen
│   │   │   │       └── route.ts
│   │   │   └── route.ts
│   │   ├── messages
│   │   │   └── route.ts
│   │   ├── register
│   │   │   └── route.ts
│   │   └── settings
│   │       └── route.ts
│   ├── components
│   │   ├── ActiveStatus.tsx
│   │   ├── Avatar.tsx
│   │   ├── AvatarGroup.tsx
│   │   ├── Button.tsx
│   │   ├── EmptyState.tsx
│   │   ├── inputs
│   │   │   ├── Input.tsx
│   │   │   └── Select.tsx
│   │   ├── modals
│   │   │   ├── GroupChatModal.tsx
│   │   │   ├── LoadingModal.tsx
│   │   │   └── Modal.tsx
│   │   └── sidebar
│   │       ├── DesktopItem.tsx
│   │       ├── DesktopSidebar.tsx
│   │       ├── MobileFooter.tsx
│   │       ├── MobileItem.tsx
│   │       ├── SettingsModal.tsx
│   │       └── Sidebar.tsx
│   ├── context
│   │   ├── AuthContext.tsx
│   │   └── ToasterContext.tsx
│   ├── conversations
│   │   ├── [conversationId]
│   │   │   ├── components
│   │   │   │   ├── Body.tsx
│   │   │   │   ├── ConfirmModal.tsx
│   │   │   │   ├── Form.tsx
│   │   │   │   ├── Header.tsx
│   │   │   │   ├── ImageModal.tsx
│   │   │   │   ├── MessageBox.tsx
│   │   │   │   ├── MessageInput.tsx
│   │   │   │   └── ProfileDrawer.tsx
│   │   │   └── page.tsx
│   │   ├── components
│   │   │   ├── ConversationBox.tsx
│   │   │   └── ConversationList.tsx
│   │   ├── layout.tsx
│   │   ├── loading.tsx
│   │   └── page.tsx
│   ├── favicon.ico
│   ├── globals.css
│   ├── hooks
│   │   ├── useActiveChannel.ts
│   │   ├── useActiveList.ts
│   │   ├── useConversation.ts
│   │   ├── useOtherUser.ts
│   │   ├── useRoutes.ts
│   │   └── useSidebar.ts
│   ├── layout.tsx
│   ├── libs
│   │   ├── prismadb.ts
│   │   └── pusher.ts
│   ├── types
│   │   └── index.ts
│   └── users
│       ├── components
│       │   ├── UserBox.tsx
│       │   └── UserList.tsx
│       ├── layout.tsx
│       ├── loading.tsx
│       └── page.tsx
├── middleware.ts
├── next.config.js
├── package-lock.json
├── package.json
├── pages
│   └── api
│       └── pusher
│           └── auth.ts
├── postcss.config.js
├── prisma
│   └── schema.prisma
├── public
│   ├── images
│   │   ├── logo.png
│   │   └── placeholder.jpg
│   ├── next.svg
│   └── vercel.svg
├── tailwind.config.js
└── tsconfig.json

33 directories, 80 files
```


## Contributing

If you would like to contribute to this project, we welcome your pull requests and contributions. Please read the contribution guidelines in the repository.

## License

This project is licensed under the [MIT License](LICENSE), which means you are free to use, modify, and distribute the code.

## Acknowledgments

We would like to express our gratitude to the developers and contributors of the libraries and tools used in this project. Their efforts have made this application possible.

Thank you for choosing the Messenger Clone project. Happy messaging!
