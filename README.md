backdoor_mmap_tools
======================

This code is still ugly, please re-write it and send pull-requests, if you want to use this.


How to use
========

* Install mmap backdoor

  `install_backdoor`

* Uninstall mmap backdoor

	`install_backdoor -u`

* Run shell with temporary root privilege.

	`run_root_shell`

* Run command "/data/local/autoexec.sh" with root privilege.

	`run_autoexec`

* Fix CVE-2013-6282 vulnerability with custom __get/put_user handlers.

	`fix_cve_2013_6282`

* Unlock fjsec LSM for Fujitsu devices.

	`unlock_lsm_fjsec`

* Unlock MIYABI LSM for SHARP devices.

	`unlock_lsm_miyabi`

* Unlock MMC protected partitions for SHARP devices.

	`unlock_mmc_protect`

* Unlock SEC LSM for SC-04E.

	`unlock_sec_sc04e`
	
* Disable TOMOYO LSM for Panasonic and LG devices.

	`disable_ccsecurity`
	
* Call reset_security_ops to disable normal LSM.

	`reset_security_ops`

* Print kernel symbols out.

	`kallsymsprint`

How to build
========

* Download and unpack android-ndk-r10e-linux-x86_64.zip from https://developer.android.com/ndk/downloads/older_releases.html

* Add to path

        `export PATH=$PATH:~/android-ndk-r10e`

* Download sources
        `git clone --recursive git@github.com:joka90/backdoor_mmap_tools.git`

* Build
       `cd backdoor_mmap_tools && ndk-build NDK_PROJECT_PATH=. APP_PLATFORM=android-15 APP_ALLOW_MISSING_DEPS=true APP_BUILD_SCRIPT=./Android.mk`

