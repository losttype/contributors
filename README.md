# Lost Type Contributors

Contributor metadata for the Lost Type Co-op, to power [losttype.com/about](http://losttype.com/about/) page _in the future_.

## Getting started

Add Lost Type’s contributor metadata to your project:

```
npm install --save losttype-contributors
```

You could then add it to your Node.js application or static site generator, for example:

```js
var contributors = require('losttype-contributors');
```

It’s also possible to move the file around with an [npm `postinstall` script](https://docs.npmjs.com/misc/scripts) in your `package.json`:

```js
"scripts": {
  "postinstall": "mv node_modules/losttype-contributors/index.json path/to/new-location/losttype-contributors.json"
}
```

Just make sure to then add the moved file to your `.gitignore` so it is installed each time, rather than becoming part of your new project’s source code.

After you’ve exposed it to your templates, you should be able to make use of it, for example:

```hbs
<ul>
  {{#each contributors }}
    <li id="{{ @key }}">
      <a href="{{{ this.url }}}">{{{ this.name }}}</a>
      <p>{{{ this.contribution }}}</p>
    </li>
  {{/each}}
</ul>
```

## Contributing

Want to add a new contributor to the Lost Type metadata? Thanks! [Click here to create a fork of the losttype/contributors repository](https://github.com/losttype/contributors/edit/master/index.json) and start editing the `index.json` metadata file.

### TODO

- Sean MacMahon
- PSY/OPS
- Amanda Gneiding
- Scotty Reifsnyder
- Connor Davenport
- Erik Hamline (Steadyprint)

## License

Available under [the MIT License](LICENSE.md) from your friends at [Lost Type](http://twitter.com/losttypecoop).

Copyright 2011–2015 © [The Lost Type Co-op](http://losttype.com)
