# Final Assignment

[![Expo](https://img.shields.io/badge/expo-1C1E24?style=for-the-badge&logo=expo&logoColor=#D04A37)](https://docs.expo.dev/) ![React Native](https://img.shields.io/badge/react_native-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB) [![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)

This is an assignment which you will be evaluated upon. Your objective is to create an app that fulfills the requirements mentioned below. Some of the requirements are mandatory to get **G** , extra requirements will get you closer to the **VG**

## App Submission

In order to deliver your code to the examiner, you have to **create your own public repository** and send the link to the examiner.

## App Description

Your task is to create a new [Expo](https://docs.expo.dev/) app using the [TypeScript template](https://docs.expo.dev/guides/typescript/#starting-from-scratch-using-a-typescript-template) that has a **product storage** where the user can add/edit and delete (CRUD) products.

The project is a system that represent a store with products. With the system the user can add new products and edit and delete existing products.

**Remarks:** the screenshots are only an example design and your final app **does not** have to look exactly like the screenshots. However, the closer it looks like it the better. You can use any UI framework you find appropriate.

### Product List Screen

The app displays an initially empty list of products (below).

<img src="./screenshots/Screenshot_1619690482.png" alt="drawing" width="200"/>

Using a FAB button (for example [this one](https://callstack.github.io/react-native-paper/fab.html)) the user can navigate to add product screen to create a new product and add it to the list so the list will look like this.

<img src="./screenshots/Screenshot_1619690519.png" alt="drawing" width="200"/>

### New Product Screen

<img src="./screenshots/Screenshot_1619690489.png" alt="drawing" width="200"/>

This screen has three fields and two buttons with fields being empty and the save button being disabled as an initial **STATE**.

- Name Field: This is mandatory field where you enter the name of the product.
- Price Field: This is a field that takes only numbers and represents the price of the product [Check Keyboard Types.](https://reactnative.dev/docs/textinput#keyboardtype)
- Product Type Field: This is a picker where you can pick the product type either **Peripheral** or **Integrated** [More about Pickers here.](https://docs.expo.dev/versions/latest/sdk/picker/)
- Save Button: It has a [Download Icon](https://icons.expo.fyi/Feather/download) and starts as disabled until the fields are filled and valid then it will be enabled.
  (More about validation below).
  Pressing the save button will add the product to the list of products and navigates back to the Items Screens.
- Cancel Button: It has a [Prohibited Icon](https://icons.expo.fyi/Foundation/prohibited) and it navigates back to Items Screen with no changes.

<img src="./screenshots/Screenshot_1619690504.png" alt="drawing" width="200"/>
<img src="./screenshots/Screenshot_1619690511.png" alt="drawing" width="200"/>

### Product Screen

You will get to this page when you select an item from the list to edit it.

From the design and functionalities should be the same as `New Product Screen` with the following exceptions:

1. The title of the page should be `"Edit Product"` or the the name of the selected product instead of `Create New Product`.
2. The fields should be initialized with data from the selected item instead of being empty
3. Saving would changes the values of the selected product and not adding a new product.

### Product Deletion

The user can delete an existing product using either an additional button on Edit screen or be more creative as seen in the `Bonus Requirements` section

<img src="./screenshots/Screenshot_1619690567.png" alt="drawing" width="200"/>

### Validation

<img src="./screenshots/Screenshot_1619690554.png" alt="drawing" width="200"/>

To be able to save a new product or changes in an existing product there are some validation rules needs to be satisfied.

1. The name of the product should be unique, you cannot create a new product with a name that is already exists in the list nor you can change the name of an existing product to a name for another product.
2. **Peripheral** products can have any price larger than $0 (zero).
3. **Integrated** products can have any price between $1000 and $2600

## Basic Requirements to get a G

You need to fulfill the following requirements to securing passing this course

1. Create the app using expo with typescript template
2. Ensure to have all the functionalities described in the `App Description` section.
3. The app should run on both ios simulator and android emulator
4. Avoid using any or untyped objects to bypass the typescript warnings
5. The product list and manipulating it should be done inside context
6. Use `useState` hook
7. Submit your code into your own repo in github
8. Use `react navigation` to move between pages
9. The app should support both English and Swedish based on the device's settings
10. Use Icons
11. The code should be structured into folders and not having it all in one file.

## Bonus requirement to reach a VG

Each requirement has points when you implement it.
You need to get at least _70_ points out of _120_ to get a VG

- Support offline mode using `asyncStorage` to store the data in the device and read from it when starting the app (10P)
- Add an authentication (i.e. login page) using firebase authentication (15P)
- Send the data to firestore and read from it with the ability to change it directly from the database and the change would appear on the app right away (10P)
- Use custom hooks for separation of concerns (5P)
- Use [swipable list](https://github.com/esthor/react-native-swipeable-list) to delete products. Unless you have a more creative way for deletion (10P)
- Create a new branch for each task you develop and use Pull Request to merge it into the main branch. (5P)
- Create some unit tests using [jest](https://jestjs.io/) (20P)
- Add back handler to edit form and warn if user goes back without saving. (5P)
- The form is validated and displays error messages for invalid data (e.g [formik](https://formik.org/docs/guides/react-native), [react-hook-forms](https://react-hook-form.com/)). (30P)
- Add a funny gif (10P)

![good luck](https://i.pinimg.com/originals/08/39/c9/0839c9b0889b853f9f90b2573465596e.gif)
