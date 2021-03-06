# yum pkg


##### Description
manage yum packages

##### Parameters

*	**`name`** (*required*): the package names and versions. You can specify multiple pakages. The following values can be used for package version:
	- ***`<null>`*** *`default`*: ensure the package is installed. If not, it will install the latest version available of all YUM repos available
	- ***`<version>`***: ensure the package is installed, at the version specified. If the version in unavailable of all YUM repos available on the host, the state will fail
	- **`<uri>`**: ensure the package will be fetched from the following uri. Warning: if one uri is specified, only packages with uri specified will be installed. *uri* can be a remote or local path to a rpm package.
	- **`latest`**: ensure the package is installed at the latest version. If a newer version is available of all YUM repos available on the host, will do upgrade automatically
	- **`removed`**: ensure the package is absent
	- **`purged`**: ensure the package is absent, and also delete all related configuration data of the package

* **`repo`** (*optional*): the repo name, which you want to use for installing the packages

		example: epel

* **`verify-gpg`** (*optional*): verify the package's GPG siganature, by default ***`true`***
				