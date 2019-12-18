Building remotely on SLAVE in workspace /data/test

 > /usr/bin/git rev-parse --is-inside-work-tree # timeout=10

Fetching changes from the remote Git repository

 > /usr/bin/git config remote.origin.url https://github.domain.com/Project-Digital/Project-eCommerce.git # timeout=10

Fetching upstream changes from https://github.domain.com/Project-Digital/Project-eCommerce.git

 > /usr/bin/git --version # timeout=10

using GIT_ASKPASS to set credentials 

Setting http proxy: mycom.domain.com:80

 > /usr/bin/git fetch --tags --progress https://github.domain.com/Project-Digital/Project-eCommerce.git +refs/heads/*:refs/remotes/origin/*

ERROR: Error fetching remote repo 'origin'

hudson.plugins.git.GitException: Failed to fetch from https://github.domain.com/Project-Digital/Project-eCommerce.git

    at hudson.plugins.git.GitSCM.fetchFrom(GitSCM.java:803)

    at hudson.plugins.git.GitSCM.retrieveChanges(GitSCM.java:1063)

    at hudson.plugins.git.GitSCM.checkout(GitSCM.java:1094)

    at hudson.scm.SCM.checkout(SCM.java:495)

    at hudson.model.AbstractProject.checkout(AbstractProject.java:1278)

    at hudson.model.AbstractBuild$AbstractBuildExecution.defaultCheckout(AbstractBuild.java:604)

    at jenkins.scm.SCMCheckoutStrategy.checkout(SCMCheckoutStrategy.java:86)

    at hudson.model.AbstractBuild$AbstractBuildExecution.run(AbstractBuild.java:529)

    at hudson.model.Run.execute(Run.java:1728)

    at hudson.model.FreeStyleBuild.run(FreeStyleBuild.java:43)

    at hudson.model.ResourceController.execute(ResourceController.java:98)

    at hudson.model.Executor.run(Executor.java:404)

Caused by: hudson.plugins.git.GitException: Command "/usr/bin/git fetch --tags --progress https://github.domain.com/Project-Digital/Project-eCommerce.git +refs/heads/*:refs/remotes/origin/*" returned status code 128:

stdout: 

stderr: error: Failed connect to github.build.ge.com:80; Operation now in progress while accessing https://github.domain.com/Project-Digital/Project-eCommerce.git/info/refs
