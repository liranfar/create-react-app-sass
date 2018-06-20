# create-react-app with sass loader
integrating .scss support in create-react-app

## Usage
```
git clone <>
cd <>
npm install
npm start
```

## Steps to reproduce from start
1. `create-react-app my-app`
1. `cd my-app`
1. `npm install --save-dev node-sass sass-loader`
1. `npm run eject`
1. in `config` directory, edit `webpack.config.dev.js` and `webpack.config.prod.js` as following:
    * inside `module` replace `test: /\.css$/` with `test: /\.scss$/`
    * between `style-loader` and `postcss-loader` objects, insert:
    ```       
              {
                loader: require.resolve('sass-loader'),
              },
    ```     

## Resources
https://www.youtube.com/watch?v=akxn6uYavf0

https://medium.com/@Connorelsea/using-sass-with-create-react-app-7125d6913760