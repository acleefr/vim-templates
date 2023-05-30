# Project Template Initialization Plugin for Vim

This Vim plugin provides functionality to initialize files using templates. It allows you to automatically insert template content and expand predefined placeholders when creating a new file.

## Prerequisites

- Vim text editor

## Installation

1. Download the plugin files and save them to a directory of your choice.

2. Open your Vim configuration file (`~/.vimrc` or `~/.config/nvim/init.vim` for Neovim).

3. Add the following lines to your configuration file:

   ```vim
   " Plugin: Project Template Initialization
   " Specify the path to the plugin files
   let g:vt_plugin_path = '/path/to/plugin/directory'

   " Load the plugin
   if !exists('g:vt_plugin_loaded')
       execute 'source ' . g:vt_plugin_path . '/vt_plugin.vim'
   endif
   ```

   Replace `/path/to/plugin/directory` with the actual path where you saved the plugin files.

4. Save the configuration file and restart Vim.

## Usage

1. Template Files:
   Create template files for different file types (e.g., `.template` files) and place them in a directory. You can specify multiple search paths for template files in the plugin configuration.

2. Placeholders:
   Inside your template files, use placeholders enclosed in double curly braces (`{{}}`) to define dynamic content. The plugin provides various predefined placeholders, such as timestamps, author details, file information, project details, etc. Refer to the code comments in the plugin file for a complete list of available placeholders.

3. Auto Initialization:
   By default, the plugin is configured to automatically initialize a new file from the corresponding template when it is created. The initialization process inserts the template content and expands the placeholders.

4. Manual Initialization:
   If you want to manually initialize a file using a template, you can use the `:TemplateInit` command followed by the template filename or extension. For example, `:TemplateInit python` initializes the current file using the `python.template` template file.

5. Placeholder Expansion:
   To manually expand all placeholders in the current file, you can use the `:TemplateExpand` command.

## Customization

The plugin provides several configuration options that you can adjust to suit your needs. Please refer to the comments in the plugin file (`vt_plugin.vim`) for details on each configuration option.

## License

This project is licensed under the [MIT License](LICENSE). You can modify and distribute it freely.