#-------------------------------------------------------------------------------------------------------------
# Copyright (c) Microsoft Corporation. All rights reserved.
# Licensed under the MIT License. See https://go.microsoft.com/fwlink/?linkid=2090316 for license information.
#-------------------------------------------------------------------------------------------------------------

# To fully customize the contents of this image, use the following Dockerfile instead:
# https://github.com/microsoft/vscode-dev-containers/tree/v0.122.1/containers/javascript-node-14/.devcontainer/Dockerfile
FROM tolgabalci/node-powershell

# ** [Optional] Uncomment this section to install additional packages. **
#
# RUN apt-get update \
#     && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

ENV OC_URL=https://mirror.openshift.com/pub/openshift-v4/clients/ocp/latest/openshift-client-linux.tar.gz
RUN wget -nv ${OC_URL} -O - | \
    tar -zxv -C /usr/local/bin/ oc \
    && chmod +x /usr/local/bin/oc

# RUN git config --global merge.tool vscode \
#     && git config --global mergetool.vscode.cmd "code --wait $MERGED" \
#     && git config --global diff.tool vscode \
#     && git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE" \
