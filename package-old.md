{
  "name": "@mikezimm/fps-lib-se",
  "version": "1.0.0",
  "description": "Library of reusable react components migrated from fps-library-v2",
  "main": "./lib/index.js",
  "types": "./lib/index.d.ts",
  "engines": {
    "node": ">=0.10.0"
  },
  "scripts": {
    "build": "del-cli \"./?(dist|lib)\" && tsc -p ./tsconfig.json && webpack",
    "package": "webpack",
    "watch": "webpack --watch",
    "start": "webpack-dev-server --config ./webpack.config.cjs",
    "clean": "del-cli \"./?(dist|lib)\"",
    "lint": "eslint ./src --ext .ts"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/fps-solutions/fps-lib-se.git"
  },
  "keywords": [
    "SPFx",
    "React Components",
    "Server Edition",
    "Subscription Edition"
  ],
  "author": "Mike Zimmerman",
  "license": "SEE LICENSE IN LICENSE.md",
  "bugs": {
    "url": "https://github.com/fps-solutions/fps-lib-se/issues"
  },
  "homepage": "https://github.com/fps-solutions/fps-lib-se#readme",
  "browserslist": [
    "last 1 version",
    "> 1%",
    "maintained node versions",
    "not dead"
  ],
  "dependencies": {
    // "@mikezimm/fps-core-v7": "^1.0.18",
    // "@mikezimm/fps-styles": "^1.0.72",

   // 2024-09-24: copied these types from default scafolded SPFx 1.4.1 React package
    "react": "15.6.2",
    "react-dom": "15.6.2",
    "react-json-view": "^1.21.3"
  },

  // 2024-09-24: copied resolutions from default scafolded SPFx 1.4.1 React package
  "resolutions": {
    "@types/react": "15.6.6"
  },
  "devDependencies": {
    "@types/node": "^14.17.6",

    // 2024-09-24: Commented these out - originals from fps-library-v2
    // "@types/react": "^17.0.45",
    // "@types/react-dom": "^17.0.17",

    // 2024-09-24: copied these types from default scafolded SPFx 1.4.1 React package
    "@types/react": "15.6.6",
    "@types/react-dom": "15.5.6",
    "@types/webpack-env": "1.13.1",

   // 2024-09-24: copied these types from from fps-core-v7/fps-library-v2
    "@types/webpack": "^5.28.0",
    "@typescript-eslint/eslint-plugin": "^5.36.2",
    "@typescript-eslint/parser": "^5.36.2",
    "del-cli": "^5.0.0",
    "eslint": "^8.23.0",
    "ts-loader": "^9.3.1",
    "typescript": "^4.7.4",
    "webpack": "^5.74.0",
    "webpack-bundle-analyzer": "^4.6.1",
    "webpack-cli": "^4.10.0",
    "webpack-dev-server": "^4.11.0"
  },
  "files": [
    "/lib",
    "LICENSE.md"
  ]
}
