# Release Notes
<!-- Do not edit this file! This file is autogenerated with -->
<!--   tools/autotag/tag_script.py                          -->

<!-- Disable lints since this is an auto-generated file.    -->
<!-- markdownlint-disable blanks-around-headers             -->
<!-- markdownlint-disable no-duplicate-header               -->
<!-- markdownlint-disable no-blanks-blockquote              -->
<!-- markdownlint-disable ul-indent                         -->
<!-- markdownlint-disable no-trailing-spaces                -->

<!-- spellcheck-disable -->

The release notes for the ROCm platform.

-------------------

## ROCm 5.6.1
<!-- markdownlint-disable first-line-h1 -->
<!-- markdownlint-disable no-duplicate-header -->

### What's New in This Release

ROCm 5.6.1 is a point release with several bug fixes in the HIP runtime.

## HIP 5.6.1 (for ROCm 5.6.1)

### Fixed Defects

* *hipMemcpy* device-to-device (intra device) is now asynchronous with respect to the host
* Enabled xnack+ check in HIP catch2 tests hang when executing tests
* Memory leak when code object files are loaded/unloaded via hipModuleLoad/hipModuleUnload APIs
* Using *hipGraphAddMemFreeNode* no longer results in a crash