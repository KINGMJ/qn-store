# Ghost Qiniu Storage

**v3.x support**

The old version follow https://github.com/minwe/qn-store

## Installation

### Via Git

In order to replace the storage module, the basic requirements are:

- Create a new folder inside `/content/adapters` called `/storage`

- Clone this repo to `/storage`

  ```
  cd [path/to/ghost]/content/adapters/storage
  git clone https://github.com/KINGMJ/qn-store
  ```

- Install dependencies

  ```
  cd qn-store
  npm install
  ```

## Configuration

In your `config.[env].json` file, you'll need to add a new `storage` block to whichever environment you want to change:

```json
{
  // ...
  "storage": {
    "active": "qn-store",
    "qn-store": {
      "accessKey": "your access key",
      "secretKey": "your secret key",
      "bucket": "your bucket name",
      "origin": "http://xx.xx.xx.glb.clouddn.com",
      "fileKey": {
        "safeString": false,
        "prefix": "YYYYMM/"
      }
    }
  }
  // ...
}
```

## License

Read [LICENSE](LICENSE)
