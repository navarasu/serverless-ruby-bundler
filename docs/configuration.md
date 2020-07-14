# Configuration

The plugin operation can be customized by specifying the `custom` configuration under `rubyLayer`. 

For example,

```yml
custom:
  rubyLayer:
    use_docker: true
    docker_yums:
      - postgresql-devel
    native_libs:
      - /usr/lib64/libpq.so.5
  ```

### Configuration Options


| Option          | Type    |  Default      |      Detail         |
| -------------   |-------- |-------------- | --------------------|
| **use_docker**  | boolean | false         | Set true to use Docker to bundle gems with OS native C extensions or system libraries |
| **docker_yums** | array   | undefined     | List of yum libraries to be preinstalled for gems which require OS native system libraries |
| **native_libs** | array   | undefined     | Paths of the native libraries files that need to be packed in lambda layer along with gems |
| **docker_file** | string  | undefined     | Path of the custom docker file to be used for bundling gems|