This repo is an experiment to setup a custo build enironment based on kirksone release for Beaglebone Black and Raspberry Pi targets.
It contains oe build environmnet initializaton scripts for the above mentioned targets.

Using this repo:
----------------
Make sure to install all the required packaes for a standard yocto build (https://docs.yoctoproject.org/ref-manual/system-requirements.html#required-packages-for-the-build-host)

1. Clone the repo.
2. git submodule init
3. git submodule update
	This gets all the sources to work with (incuding meta-jsr, a custom layer for dev)
4. source oe-init-build-env-[bbb/rpi]
5. update the locale settins if needed (https://stackoverflow.com/questions/14547631/python-locale-error-unsupported-locale-setting)
6. Modify the bblayers.conf
	update the BBLAYERS variable with appropriate path for the layers.
	(#TODO :Update the oe-init-build-env-* scripts to properly set the BBLAYERS variable while sourcing)
7. Modify the local.conf (if needed)
	By default, the "downloads" directory will be created under ${HOME}/yocto. Change this if needed.
8. Run the desired bitbake target



#TODO:
1. Automate the locale update in oe-init-build-env-* scripts.
2. Jenkins pipeline (or workflow) to trigger a build.

