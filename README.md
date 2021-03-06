# AzureDocumentDbTypeProvider

This project aims to provide an F# Type Provider to enable easy access to the Azure DocumentDb service.

## Contributing

Contributions are welcome. Anyone is welcome to log an issue, a pull request or message me on GitHub.

### Building the library

The project's tests depend on having access to a test account. In order to be able to use the build script you will need to provide access credentials to a valid DocumentDb account. 
This can be done in one of 2 ways:

* Add environment variables 'TEST_ACC_URI' & 'TEST_ACC_KEY' to your build machine with the uri and key from the Azure Portal
* Edit the TestAccountConfig.fs file to provide the necessary credentials

If you elect to set environment variables then the build script will replace the literal values in TestAccountConfig.fs before building.

The integration tests will first set up a couple of databases named test1 and test2 then run the tests before deleting these databases again. **Please note this process will delete any existing databases in your account named test1 or test2**

The project uses Paket to manage dependencies and FAKE to control the build. You should be able to build the library by running the *build.bat* file in the root of the repository. If you encounter any problems doing so please report an issue.  
