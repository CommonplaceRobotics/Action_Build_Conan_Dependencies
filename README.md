# Action_Build_Conan_Dependencies
Github Action for building Conan 2 dependencies

This action is intended to be used for CPR internal purposes. Use by anyone else is at your own risk, consider this repository not stable.

```yaml
- uses: CommonplaceRobotics/Action_Build_Conan_Dependencies/Linux_x86_64@v1
  with:
	lockfile: 'conan_linux.lock'
	cache_key: conan-${{ runner.os }}-${{ hashFiles('**/conan_linux.lock', '**/conanfile.py') }}
```

```yaml
- uses: CommonplaceRobotics/Action_Build_Conan_Dependencies/Linux_armv8_32@v1
  with:
	lockfile: 'conan_linux.lock'
	cache_key: conan-${{ runner.os }}-${{ hashFiles('**/conan_linux.lock', '**/conanfile.py') }}
```

```yaml
- uses: CommonplaceRobotics/Action_Build_Conan_Dependencies/Windows@v1
  with:
	lockfile: 'conan_windows.lock'
	cache_key: conan-${{ runner.os }}-${{ hashFiles('**/conan_windows.lock', '**/conanfile.py') }}
```