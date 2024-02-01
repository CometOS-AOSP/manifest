# 🌠 CometOS
A custom ROM for mobile devices, based on AOSP, offering essential AI features, security, performance, and a user experience close to stock.

## Getting Started

To begin, ensure you have a solid understanding of Git and Repo.

## Syncing the Repositories:

To synchronize the repositories, use the following commands:

```bash
repo init -u https://github.com/CometOS-AOSP/manifest.git -b UpsideDownCake/ultracosmic --git-lfs
```

Then sync up:

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

## > Building the System
- Before initiating the build process, it's *crucial* to set up the ROM environment using the `envsetup.sh` script. 
- Execute the following command:

```bash
source build/envsetup.sh
```

### > Android Build Types

In the context of building Android ROMs or software using the Android Open Source Project (AOSP), there are three primary build types, each serving a different purpose:

#### 1. Eng (Engineering) Build:

- Designed for developers and engineers working on the Android source code.
- Includes additional debugging information, development tools, and features for troubleshooting and profiling.
- Eng builds are larger in size and may not be optimized for performance but provide extensive tools and information for debugging and development purposes.

#### 2. Userdebug Build:

- A step closer to a production or user release compared to the eng build.
- Retains some debugging information and development tools, making it useful for developers and testers.
- Userdebug builds are smaller than eng builds but still include debugging capabilities, suitable for testing and identifying issues.

#### 3. User Build:

- The most streamlined and optimized version intended for end-users.
- Does not include debugging tools or additional development features present in eng and userdebug builds.
- User builds are the smallest in size and focus on providing a stable and efficient user experience without the overhead of debugging tools.

### > Device Codenames
- It can be according to the device trees you have
  
```bash
lunch comet_CODENAME-BUILDTYPE
```
Ex: ```lunch comet_marble-userdebug```

### > Let's start compilation of UpsideDownCake(Android 14)!!!
#### make: 
- General-purpose build tool used in many projects, including Android. Used to build specific modules or components.

#### mka (Make Alternative):
- Android-specific wrapper around make. Simplifies the build process by handling environment setup and flags. Convenient and faster for building Android OS.
```bash
make bacon -j$(nproc --all)
```
**or**
```bash
mka bacon -j$(nproc --all)
```
