# eslint-config
ESLint Configuration Tutorial

## Installation
```shell
npm i eslint -D
```
or
```shell
yarn add eslint -D
```

## Configuration
Create the **.eslintrc.json** file at the root of the project and then create an object with the key **extends** and fill its value with an array containing the style guide you intend to adopt for the project's code.
```json
{
    "extends": [
        "airbnb",
    ]
}
```

## VS Code Extension
In **Extensions** in **VS Code**, search for the **dbaeumer.vscode-eslint** extension and install it.

> You can also create the **.vscode/extensions.json** file at the root of the project so that VS Code suggests installing this extension. Add the following content:
```json
{
    "recommendations": [
        "dbaeumer.vscode-eslint"
    ]
}
```

## Enabling Fix on Save
To enable auto fix on save, create the **.vscode/settings.json** file at the root of the project with the following content:

> You can also enable it for all projects opened with VS Code by adding the same content to the global VS Code configuration.

```json
{
    "editor.codeActionsOnSave": {
        "source.fixAll.eslint": "always"
    }
}
```

## Mass Fix
To apply ESLint fixes to all project files, run the following command:

> Pay attention to the file extensions in the command and modify them if necessary.

```shell
eslint src --ext .js,.ts,.tsx --fix
```
