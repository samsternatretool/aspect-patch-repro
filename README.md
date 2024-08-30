# aspect-patch-repro

To reproduce the bug:
```
bazel build :node_modules
```

You should see:
```
INFO: Repository aspect_rules_js~~npm~npm_deps__at_reduxjs_toolkit__1.9.7__b7ns7wotak7hxwozlinknj3bsa instantiated at:
  <builtin>: in <toplevel>
Repository rule npm_import_rule defined at:
  /private/var/tmp/_bazel_samstern/698bf36c5bafaeb260af390d4abf96d6/external/aspect_rules_js~/npm/private/npm_import.bzl:865:34: in <toplevel>
INFO: repository @@aspect_rules_js~~npm~npm_deps__at_reduxjs_toolkit__1.9.7__b7ns7wotak7hxwozlinknj3bsa' used the following cache hits instead of downloading the corresponding file.
 * Hash 'b7bbfc64fc6184a80e2ad53ebb2253d7796ee2f2fb6b3e5a162e087680ecfde4b9e3c79d9f633c224f61f1fc60bcc8c6a00515152b7a642d4fe5c5a6434d7841' for https://registry.npmjs.org/@reduxjs/toolkit/-/toolkit-1.9.7.tgz
If the definition of 'repository @@aspect_rules_js~~npm~npm_deps__at_reduxjs_toolkit__1.9.7__b7ns7wotak7hxwozlinknj3bsa' was updated, verify that the hashes were also updated.
ERROR: An error occurred during the fetch of repository 'aspect_rules_js~~npm~npm_deps__at_reduxjs_toolkit__1.9.7__b7ns7wotak7hxwozlinknj3bsa':
   Traceback (most recent call last):
        File "/private/var/tmp/_bazel_samstern/698bf36c5bafaeb260af390d4abf96d6/external/aspect_rules_js~/npm/private/npm_import.bzl", line 506, column 10, in _npm_import_rule_impl
                patch(rctx, patch_args = rctx.attr.patch_args, patch_directory = _EXTRACT_TO_DIRNAME)
        File "/private/var/tmp/_bazel_samstern/698bf36c5bafaeb260af390d4abf96d6/external/aspect_bazel_lib~/lib/private/patch.bzl", line 141, column 21, in patch
                fail(msg)
Error in fail: Error applying patch @@//:patches/@reduxjs__toolkit@1.9.7.patch:
patching file 'dist/query/react/rtk-query-react.umd.js'
patching file 'dist/query/react/rtk-query-react.umd.js.map'
patching file 'dist/query/rtk-query.cjs.development.js'
patching file 'dist/query/rtk-query.cjs.development.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.cjs.development.js.map.rej'
patching file 'dist/query/rtk-query.cjs.production.min.js'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.cjs.production.min.js.rej'
patching file 'dist/query/rtk-query.cjs.production.min.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.cjs.production.min.js.map.rej'
patching file 'dist/query/rtk-query.esm.js'
patching file 'dist/query/rtk-query.esm.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.esm.js.map.rej'
patching file 'dist/query/rtk-query.modern.development.js'
patching file 'dist/query/rtk-query.modern.development.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.development.js.map.rej'
patching file 'dist/query/rtk-query.modern.js'
patching file 'dist/query/rtk-query.modern.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.js.map.rej'
patching file 'dist/query/rtk-query.modern.production.min.js'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.production.min.js.rej'
patching file 'dist/query/rtk-query.modern.production.min.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.production.min.js.map.rej'
patching file 'dist/query/rtk-query.umd.js'
patching file 'dist/query/rtk-query.umd.js.map'
patching file 'src/query/createApi.ts'
ERROR: no such package '@@aspect_rules_js~~npm~npm_deps__at_reduxjs_toolkit__1.9.7__b7ns7wotak7hxwozlinknj3bsa//': Error applying patch @@//:patches/@reduxjs__toolkit@1.9.7.patch:
patching file 'dist/query/react/rtk-query-react.umd.js'
patching file 'dist/query/react/rtk-query-react.umd.js.map'
patching file 'dist/query/rtk-query.cjs.development.js'
patching file 'dist/query/rtk-query.cjs.development.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.cjs.development.js.map.rej'
patching file 'dist/query/rtk-query.cjs.production.min.js'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.cjs.production.min.js.rej'
patching file 'dist/query/rtk-query.cjs.production.min.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.cjs.production.min.js.map.rej'
patching file 'dist/query/rtk-query.esm.js'
patching file 'dist/query/rtk-query.esm.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.esm.js.map.rej'
patching file 'dist/query/rtk-query.modern.development.js'
patching file 'dist/query/rtk-query.modern.development.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.development.js.map.rej'
patching file 'dist/query/rtk-query.modern.js'
patching file 'dist/query/rtk-query.modern.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.js.map.rej'
patching file 'dist/query/rtk-query.modern.production.min.js'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.production.min.js.rej'
patching file 'dist/query/rtk-query.modern.production.min.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.production.min.js.map.rej'
patching file 'dist/query/rtk-query.umd.js'
patching file 'dist/query/rtk-query.umd.js.map'
patching file 'src/query/createApi.ts'
ERROR: /Users/samstern/Projects/aspect-patch-repro/BUILD:3:22: //:.aspect_rules_js/node_modules/@reduxjs+toolkit@1.9.7_b7ns7wotak7hxwozlinknj3bsa/lc depends on @@aspect_rules_js~~npm~npm_deps__at_reduxjs_toolkit__1.9.7__b7ns7wotak7hxwozlinknj3bsa//:pkg in repository @@aspect_rules_js~~npm~npm_deps__at_reduxjs_toolkit__1.9.7__b7ns7wotak7hxwozlinknj3bsa which failed to fetch. no such package '@@aspect_rules_js~~npm~npm_deps__at_reduxjs_toolkit__1.9.7__b7ns7wotak7hxwozlinknj3bsa//': Error applying patch @@//:patches/@reduxjs__toolkit@1.9.7.patch:
patching file 'dist/query/react/rtk-query-react.umd.js'
patching file 'dist/query/react/rtk-query-react.umd.js.map'
patching file 'dist/query/rtk-query.cjs.development.js'
patching file 'dist/query/rtk-query.cjs.development.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.cjs.development.js.map.rej'
patching file 'dist/query/rtk-query.cjs.production.min.js'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.cjs.production.min.js.rej'
patching file 'dist/query/rtk-query.cjs.production.min.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.cjs.production.min.js.map.rej'
patching file 'dist/query/rtk-query.esm.js'
patching file 'dist/query/rtk-query.esm.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.esm.js.map.rej'
patching file 'dist/query/rtk-query.modern.development.js'
patching file 'dist/query/rtk-query.modern.development.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.development.js.map.rej'
patching file 'dist/query/rtk-query.modern.js'
patching file 'dist/query/rtk-query.modern.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.js.map.rej'
patching file 'dist/query/rtk-query.modern.production.min.js'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.production.min.js.rej'
patching file 'dist/query/rtk-query.modern.production.min.js.map'
1 out of 1 hunks failed--saving rejects to 'dist/query/rtk-query.modern.production.min.js.map.rej'
patching file 'dist/query/rtk-query.umd.js'
patching file 'dist/query/rtk-query.umd.js.map'
patching file 'src/query/createApi.ts'
ERROR: Analysis of target '//:node_modules' failed; build aborted: Analysis failed
INFO: Elapsed time: 1.000s, Critical Path: 0.00s
INFO: 1 process: 1 internal.
ERROR: Build did NOT complete successfully
```