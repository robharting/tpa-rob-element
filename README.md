[![Build Status](https://travis-ci.org/ING-Group/tpa-rob-element.svg?branch=master)](https://travis-ci.org/ING-Group/tpa-rob-element)

# tpa-rob-element

An element providing a starting point for your own reusable TPA elements.


## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Linting Your Element

If you wish to lint your element, we recommend that you use
[Polylint](https://github.com/PolymerLabs/polylint) to take into account Polymer 
linting specificities. You can install it via:

    npm install -g polylint

And you can run it via:

	polylint -i tpa-rob-element.html

If your element contains errors, they will appear on the console.

Note that it is possible to use `Polylint` with Atom and Sublime with the appropriate package/plugin.

For more options regarding `polylint`, please refer to the 
[documentation](https://github.com/PolymerLabs/polylint#polylint).


## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    gulp
    
Do not run via `polyserve`, as it will not include the API mocking host

Once running, you can preview your element at
`http://localhost:8080/components/tpa-rob-element/`, where `tpa-rob-element` is the name of the directory containing it.

### API Blueprint

Hosting [API Blueprint](https://apiblueprint.org/) mocks is provided via [Drakov](https://github.com/Aconex/drakov/)

The hosting of the mocks combined with `polyserve` is via [Proxy Middleware](https://github.com/chimurai/http-proxy-middleware/)

## Testing Your Element

Simply navigate to the `/test` directory of your element to run its tests. If
you are using Polyserve: `http://localhost:8080/components/tpa-rob-element/test/`

### web-component-tester

The tests are compatible with [web-component-tester](https://github.com/Polymer/web-component-tester).
Install it via:

    npm install -g web-component-tester-istanbul

Then, you can run your tests on _all_ of your local browsers via:

    wct
    
Code coverage is provided by [Istanbul](https://github.com/thedeeno/web-component-tester-istanbul)

    npm install -g web-component-tester-istanbul

#### WCT Tips

`wct -l chrome` will only run tests in chrome.

`wct -p` will keep the browsers alive after test runs (refresh to re-run).

`wct test/some-file.html` will test only the files you specify.


## Yeoman support

If you'd like to use Yeoman to scaffold your element that's possible. The TPA [`generator-tpa`](https://github.com/ING-Group/generator-tpa) generator has a [`tpa`](https://github.com/ING-Group/generator-tpa#tpa) subgenerator.
