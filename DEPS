use_relative_paths = True

# Dependencies on outside packages.
#
deps = {
  "common": "https://skia.googlesource.com/common.git@0ad95c13aaab3bbb89a97952b83c915d470681df",
  # TODO(epoger): Whenever you update the hash of the "common" repo above,
  # update the following transitive dependencies as well...
  # (I tried to use From() to import the revision numbers from
  # common's DEPS file, but that caused "gclient sync" to block forever.)
  #
  # Once we fix http://crbug.com/393000 ('Gclient recursedeps feature
  # doesn't seem to respect use_relative_paths'), we can import them
  # recursively, like so:
  #   recursedeps = {"common"}
  "common/third_party/externals/google-api-python-client" : "https://github.com/google/google-api-python-client.git@ecc64a0a2baa4a77f35dec83ad05c6c9ba2d2841",
  "common/third_party/externals/httplib2" : "https://github.com/jcgregorio/httplib2.git@7d1b88a3cf34774242bf4c0578c09c0092bb05d8",
  "common/third_party/externals/oauth2client" : "https://github.com/google/oauth2client.git@d02b317af0313dcf66755844f5421651af5eb356",
  "common/third_party/externals/uritemplate-py" : "https://github.com/uri-templates/uritemplate-py.git@1e780a49412cdbb273e9421974cb91845c124f3f",

  # DEPS using https://chromium.googlesource.com are pulled from chromium @ r205199
  # (see https://chromium.googlesource.com/chromium/chromium/+/c59bfa8ef877f45bfa859669053859857af1d279)
  "third_party/externals/angle2" : "https://chromium.googlesource.com/angle/angle.git@23a8a433529d9db23882c702a29d5e594841563d",
  "third_party/externals/freetype" : "https://skia.googlesource.com/third_party/freetype2.git@VER-2-5-0-1",
  "third_party/externals/gyp" : "https://chromium.googlesource.com/external/gyp.git@3917682a16d5c19ff3576a8be0ffdb3a332954b1",
  "third_party/externals/libjpeg" : "https://chromium.googlesource.com/chromium/deps/libjpeg_turbo.git@82ce8a6d4ebe12a177c0c3597192f2b4f09e81c3",
  "third_party/externals/jsoncpp" : "https://chromium.googlesource.com/external/jsoncpp/jsoncpp.git@ab1e40f3bce061ea6f9bdc60351d6cde2a4f872b",
  # Move to a webp version newer than 0.3.0 to pickup NEON fix for iOS
  "third_party/externals/jsoncpp-chromium" : "https://chromium.googlesource.com/chromium/src/third_party/jsoncpp.git@41239939c0c60481f34887d52c038facf05f5533",
  "third_party/externals/libwebp" : "https://chromium.googlesource.com/webm/libwebp.git@3fe91635df8734b23f3c1b9d1f0c4fa8cfaf4e39",
  # "third_party/externals/v8" : "git://github.com/v8/v8.git@d15b0f0f2099dbd72867f3df70e9aaf5b8afbd2c",
  "third_party/externals/nanomsg": "git://github.com/nanomsg/nanomsg.git@0.4-beta",
}

deps_os = {
  "android": {
    "platform_tools/android/third_party/externals/expat" : "https://android.googlesource.com/platform/external/expat.git@android-4.2.2_r1.2",
    "platform_tools/android/third_party/externals/gif" : "https://android.googlesource.com/platform/external/giflib.git@android-4.2.2_r1.2",
    "platform_tools/android/third_party/externals/png" : "https://android.googlesource.com/platform/external/libpng.git@android-4.2.2_r1.2",
    "platform_tools/android/third_party/externals/jpeg" :
      "https://android.googlesource.com/platform/external/jpeg.git@746f1f0853ddbd14ab5da6af35cc1fa560453d1e",
  },
  "chromeos": {
    "platform_tools/chromeos/third_party/externals/gif" : "https://android.googlesource.com/platform/external/giflib.git@android-4.2.2_r1.2",
    "platform_tools/chromeos/toolchain/src/third_party/chromite": "https://chromium.googlesource.com/chromiumos/chromite.git@d6a4c7e0ee4d53ddc5238dbddfc0417796a70e54",
    "platform_tools/chromeos/toolchain/src/third_party/pyelftools": "https://chromium.googlesource.com/chromiumos/third_party/pyelftools.git@bdc1d380acd88d4bfaf47265008091483b0d614e",
  },

  # barelinux is a DEPS target that has no shared libraries to link
  # to, similar to android or chromeos.
  "barelinux": {
    "third_party/externals/giflib" :
      "https://android.googlesource.com/platform/external/giflib.git@android-4.2.2_r1.2",
    "third_party/externals/libpng" :
       "https://android.googlesource.com/platform/external/libpng.git@android-4.2.2_r1.2",
    "third_party/externals/zlib" :
       "https://android.googlesource.com/platform/external/zlib.git@android-4.2.2_r1.2",
  }
}

#hooks = [
#  {
#    # A change to a .gyp, .gypi, or to GYP itself should run the generator.
#    "pattern": ".",
#    "action": ["python", "trunk/gyp_skia"],
#  },
#]