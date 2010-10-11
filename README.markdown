`sprockets-rails`
=================

This a modified version of sprockets-rails, allwowing it to be used as rails 3 engine.

1. Just require it in your gemfile

2. Edit your `config/routes.rb` file to add routes for `SprocketsController`:

        ActionController::Routing::Routes.draw do |map|
          # Add the following line:
          SprocketsApplication.routes(map)
          ...
        end

3. Move your JavaScript source files from `public/javascripts/` into `app/javascripts/`. All files in all subdirectories of `app/javascripts/` will be required by Sprockets in alphabetical order, with the exception of `app/javascripts/application.js`, which is required _before any other file_. (You can change this behavior by editing the `source_files` line of `config/sprockets.yml`.)

4. Adjust your HTML templates to call `<%= sprockets_include_tag %>` instead of `<%= javascript_include_tag ... %>`.

Once `sprockets-rails` is installed, you can check out Sprockets plugins into the `vendor/sprockets/` directory. By default, `sprockets-rails` configures Sprockets' load path to search `vendor/sprockets/*/src/`, as well as `vendor/plugins/*/javascripts/`. This means that the `javascripts/` directories of Rails plugins are automatically installed into your Sprockets load path.

## License

Copyright &copy; 2009 Sam Stephenson.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

