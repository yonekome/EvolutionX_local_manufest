local_manifests

Custom manifest for my unofficial Evolution X build.
Sync

# Initialize local repository
repo init -u https://github.com/Evolution-X/manifest -b tiramisu

# Clone my custom manifest
git clone -b tiramisu https://github.com/nattolecats/local_manifests .repo/local_manifests

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

Build

# Set up environment
. build/envsetup.sh

# Choose a target
lunch evolution_denniz-userdebug

# Build the code
